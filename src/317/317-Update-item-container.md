# Update item container
Updates the items in a given interface component.

## Packet Details
| Key | Value |
|--|--|
| Name | Update item container |
| Description | Updates items in an interface component. |
| Opcode | 53 |
| Type | VARIABLE_SHORT |
| Length | N/A |
| Revision | 317 |

## Packet Structure
| Data Type | Description |
|--|--|
| Unsigned [Short](/Data-Types.html#common-data-types) | Interface ID. |
| Unsigned [Short](/Data-Types.html#common-data-types) | Amount of items. |

The rest in pseudo-code:

```java
for (i = 0; i < amt_of_items; i++) {
    item_amount = read_u_byte(); // Item Amount: U Byte
    
    if (item_amount == 255)
        item_amount = read_int_me_b(); // Item Amount (if entered as 255 previously - to allow bigger amounts than 254): Middle-Endian Big Integer

    item_id = read_u_short_le_a(); // Item ID: U Short Little Endian Special A
}
```
