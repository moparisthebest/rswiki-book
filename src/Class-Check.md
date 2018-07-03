# Class check

The class check originated with the new Runescape engine update which
took place around the 4xx revisions.
It gives the Jagex servers the ability to check the modifiers, update,
or fetch the value for a field.
It also gives functionality to invoke a method with parameters and get
it's return value, or check it's modifiers.
Each of these functionalities are described with a request type.
A class check request is built up with many of these request types.
Each request is tagged with an unique id.

## Request format

```
unsigned byte numberOfRequests;
int uid;
byte[] requests_block;
```

The `requests_block` is comprised of multiple requests, each with the following format:

```
unsigned byte type;
type-dependent data;
```

## Response format

```
int uid;
byte[] responses_block;
short payloadCrc;
```

The `responses_block` is comprised of multiple responses, each with the following format:

```
byte responseCode;
type-dependent data;
```

## Request Types

For request types 0, 2, 4 there will only be one successful response
code and a short value of the value being requested will be sent.
For request type 1, only the successful response code will be used but no
value will be sent back.

| Opcode | Name | Description |
|---|---|---|
| 0 | Fetch fumeric field  | Fetches the value of a numeric field. |
| 1 | Update numeric field | Updates the value of a numeric field. |
| 2 | Get field modifiers | Gets the modifiers of a field.  |
| 3 | Invoke method | Invokes a method and sends back its return object.  |
| 4 | Get method modifiers | Gets the modifiers of a method.  |

## Return Codes

For opcode 0, there are cases where a numeric value is sent to the server
on fetch requests.
This value is always a short.

For a method invoke request, there isn't a value that is sent to the server.
It is just assumed that there wasn't a return object from the invoked method.

| Opcode | Name | On Receive/Response | Description |
|---|---|---|---|
| 0 | Successful | Response | Successfully executed the request. |
| 1 | Successful - Returned numeric value | Response | Successfully executed the request, and returned a numeric value. |
| 2 | Successful - Returned string value | Response | Successfully executed the request, and returned a string value. |
| 4 | Successful - Returned object value | Response | Successfully executed the request, and returned an object value. |
| -1 | ClassNotFoundException | Receive | A ClassNotFoundException was thrown while receiving a request from the server. |
| -2 | SecurityException | Receive | A SecurityException was thrown while receiving a request from the server. |
| -3 | NullPointerException | Receive | A NullPointerException was thrown while receiving a request from the server. |
| -4 | Exception | Receive | An Exception was thrown while receiving a request from the server. |
| -5 | Throwable | Receive | An error or exception was thrown while receiving a request from the server. |
| -10 | ClassNotFoundException | Response | A ClassNotFoundException was thrown while responding to a request from the server. |
| -11 | InvalidClassException | Response | An InvalidClassException was thrown while responding to a request from the server. |
| -12 | StreamCorruptedException | Response | A StreamCorruptedException was thrown while responding to a request from the server. |
| -13 | OptionDataException | Response | An OptionDataException was thrown while responding to a request from the server. |
| -14 | IllegalAccessException | Response | An IllegalAccessException was thrown while responding to a request from the server. |
| -15 | IllegalArgumentException | Response | An IllegalArgumentException was thrown while responding to a request from the server. |
| -16 | InvocationTargetException | Response | An InvocationTargetException was thrown while responding to a request from the server. |
| -17 | SecurityException | Response | A SecurityException was thrown while responding to a request from the server.  |
| -18 | IOException | Response | An IOException was thrown while responding to a request from the server. |
| -19 | NullPointerException | Response | A NullPointerException was thrown while responding to a request from the server. |
| -20 | Exception | Response | An Exception was thrown while responding to a request from the server.  |
| -21 | Throwable | Response | An error or exception was thrown while receiving a request from the server.  |
