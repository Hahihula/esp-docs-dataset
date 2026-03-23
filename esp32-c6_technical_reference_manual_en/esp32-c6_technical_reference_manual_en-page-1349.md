

```markdown
Register 38.3. PARL_IO_TX_CFGO_REG (0x0008)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | PARL_IO_TX_FIFO_SRST                                                       |
| 29  | PARL_IO_TX_BUS_WID_SEL                                                     |
| 28  | PARL_IO_TX_BIT_UNPACK_ORDER                                                |
| 27  | PARL_IO_TX_SMP_EDGE_SEL                                                    |
| 26  | (reserved)                                                                  |
| 25  | PARL_IO_TX_HW_VALID_EN                                                     |
| 24  | PARL_IO_TX_START                                                            |
| 23  | (reserved)                                                                  |
| 22  | PARL_IO_TX_BYTELEN                                                          |
| 21  | (reserved)                                                                  |
| 20  | O                                                                            |
| 19  | O                                                                            |
| 18  | O                                                                            |
| 17  | O                                                                            |
| 16  | O                                                                            |
| 15  | O                                                                            |
| 14  | O                                                                            |
| 13  | O                                                                            |
| 12  | O                                                                            |
| 11  | O                                                                            |
| 10  | O                                                                            |
| 9   | O                                                                            |
| 8   | O                                                                            |
| 7   | O                                                                            |
| 6   | O                                                                            |
| 5   | O                                                                            |
| 4   | O                                                                            |
| 3   | O                                                                            |
| 2   | O                                                                            |
| 1   | O                                                                            |
| 0   | Reset                                                                       |

PARL_IO_TX_BYTELEN Configures the byte length of the data sent by TX. (R/W)

PARL_IO_TX_START Configures whether to start TX global data output.
O: No effect
1: Start
(R/W)

PARL_IO_TX_HW_VALID_EN Configures whether to enable TX hardware data valid signal.
O: Disable
1: Enable
(R/W)

PARL_IO_TX_SMP_EDGE_SEL Configures whether to invert the TX output clock
O: Not invert
1: Invert (R/W)

PARL_IO_TX_BIT_UNPACK_ORDER Configures the unpacking order to unpack bits from 1 byte when data bus width is 4/2/1 bit.
O: Unpack from MSB
1: Unpack from LSB
(R/W)

PARL_IO_TX_BUS_WID_SEL Configures TX data bus width.
O: 16 bit
1: 8 bit
2: 4 bit
3: 2 bit
4: 1 bit
(R/W)

Continued on the next page...
```