# Camera oscillate
Begins camera oscillation, which is implemented using a configurable sinusoidal oscillator to offset a specific degree of freedom.

## Packet Details
| Key | Value |
|--|--|
| Name | Camera oscillate |
| Description | Begin camera oscillation. |
| Opcode | 35 |
| Type | Fixed |
| Length | 4 |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| [Byte](/Data-Types.html#common-data-types) | Parameter (camera X, Z, Y, yaw, pitch) |
| [Byte](/Data-Types.html#common-data-types) | Jitter (for randomization) |
| [Byte](/Data-Types.html#common-data-types) | Amplitude |
| [Byte](/Data-Types.html#common-data-types) | Frequency (scaled by 100) |

## Other Information
The oscillate event enables the client to oscillate one of 5 of it's position parameters.
i.e. corresponding to the camera's degrees of freedom; parameters 0, 1, and 2 refer to the location of the camera, while 3 and 4 deal with the camera's orientation.
Together, these enable complex effects involving manipulation of the camera position to give rise to simulated earth-quakes and camera shock.

| Parameter | Description |
|--|--|
| 0 | Camera location along world X axis (a horizontal axis, aligned with map grid X) |
| 1 | Camera location along world Z axis (vertical axis) |
| 2 | Camera location along world Y axis (a horizontal axis, aligned with map grid Y) |
| 3 | Camera orientation in world X plane w.r.t. world Z axis, i.e. yaw |
| 4 | Camera orientation in world Z plane w.r.t. world X axis, i.e. pitch |

Note there is no built-in way to manipulate camera roll, as this is not one of the camera's degrees of freedom.

## What it's doing
Every time the world is rendered, each camera parameter that is enabled for oscillation is offset by a value computed as follows:

| Calculation | Formula |
|--|--|
| Delta | `(int) ((Math.random() * (double) (jitter * 2 + 1) - (double) jitter) + Math.sin((double) phase * ((double) frequency / 100D)) * (double) amplitude);` |

Each parameter's phase accumulator (phase) is incremented by 1 each logic update.

## Parameter
The offset itself is detailed as follows for each parameter:

| Parameter | Action |
|--|--|
| 0 | `camera_x += delta` |
| 1 | `camera_z += delta` |
| 2 | `camera_y += delta` |
| 3 | `camera_yaw = camera_yaw + delta & 0x7ff;` |
| 4 | `camera_pitch += delta` |

Note that the camera's yaw is corrected modulo 0x7ff, or 2048, which is equivalent to 2 \pi radians in Jagex's binary angle system.
This is not done to the camera pitch, which is instead clamped (see below).

## Note
For oscillating the camera pitch, clamping is done to ensure the angle not out of bounds:

```java
if (camera_pitch < 128)
    camera_pitch = 128
if (camera_pitch > 383)
    camera_pitch = 383
```

This is due to Jagex restricting the possible range of orientations the camera may take.
