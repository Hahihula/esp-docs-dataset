

```markdown
Register 38.21. TWAIFD_RX_STATUS_RX_SETTINGS_REG (0x0068)

| Bit | Field Name      | Description                                                                 |
|-----|-----------------|-----------------------------------------------------------------------------|
| 31  | (reserved)      |                                                                             |
| 17  | TWAIFD_RTSOP    | (reserved)                                                                   |
| 16  |                 |                                                                             |
| 15  |                 |                                                                             |
| 14  | TWAIFD_RXFRC    | TWAIFD_RXF Represents whether the RX buffer is full.                         |
|     |                 | O: Not full                                                                  |
|     |                 | 1: Full                                                                      |
| (RO)|                 |                                                                             |
| 4   | (reserved)      |                                                                             |
| 3   | TWAIFD_RXMOF    | Represents the number of received frames in the RX buffer. RXMOF represents the RX buffer is in the middle of reading a frame. When the field is 1, the next read from TWAIFD_RX_DATA will return a word other than the first word (FRAME_FORMAT_W) of the CAN frame. (RO) |
| 2   | TWAIFD_RXE      | Represents whether the RX buffer is empty.                                   |
|     |                 | O: Not empty                                                                 |
|     |                 | 1: Empty                                                                     |
| (RO)|                 |                                                                             |
| 1   | TWAIFD_RXF      | Represents the number of CAN frames currently stored in the RX buffer. (RO)    |
| 0   | Reset           |                                                                             |

TWAIFD_RXE Represents whether the RX buffer is empty.
O: Not empty
1: Empty
(RO)

TWAIFD_RXF Represents whether the RX buffer is full.
O: Not full
1: Full
(RO)

TWAIFD_RXMOF Represents the number of received frames in the RX buffer. RXMOF represents the RX buffer is in the middle of reading a frame. When the field is 1, the next read from TWAIFD_RX_DATA will return a word other than the first word (FRAME_FORMAT_W) of the CAN frame. (RO)

TWAIFD_RXFRC Represents the number of CAN frames currently stored in the RX buffer. (RO)

TWAIFD_RTSOP Represents the RX buffer timestamp option. Modify only when TWAIFD_ENA = 0.
O: RTS_END - The timestamp of the received frame in the RX FIFO is captured in the last bit of the EOF field.
1: RTS_BEG - The timestamp of the received frame in the RX FIFO is captured in the SOF field.
(R/W)
```