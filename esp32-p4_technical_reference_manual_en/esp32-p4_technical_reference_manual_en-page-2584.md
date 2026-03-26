

```markdown
Register 51.11. USB_SERIAL_JTAG_SER_AFIFO_CONFIG_REG (0x0064)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30-29| USB_SERIAL_JTAG_SERIAL_IN_AFIFO_WFULL     | Represents CDC_ACM IN async FIFO full signal in write clock domain. (RO)    |
| 28  | USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_REMPTY   | Represents CDC_ACM OUT async FIFO empty signal in read clock domain. (RO)   |
| 27-26| USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_RD | Configures whether to reset CDC_ACM OUT async FIFO read clock domain.      |
|     |                                          | 0: No effect                                                                |
|     |                                          | 1: Reset                                                                    |
| (R/W)|                                          |                                                                             |
| 25-24| USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_WR | Configures whether to reset CDC_ACM OUT async FIFO write clock domain.      |
|     |                                          | 0: No effect                                                                |
|     |                                          | 1: Reset                                                                    |
| (R/W)|                                          |                                                                             |
| 23-22| USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_RD  | Configures whether to reset CDC_ACM IN async FIFO read clock domain.        |
|     |                                          | 0: No effect                                                                |
|     |                                          | 1: Reset                                                                    |
| (R/W)|                                          |                                                                             |
| 21-20| USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_WR  | Configures whether to reset CDC_ACM IN async FIFO write clock domain.       |
|     |                                          | 0: No effect                                                                |
|     |                                          | 1: Reset                                                                    |
| (R/W)|                                          |                                                                             |

```
```plaintext
USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_WR   Configures whether to reset CDC_ACM IN async FIFO write clock domain.
0: No effect
1: Reset
(R/W)

USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_RD   Configures whether to reset CDC_ACM IN async FIFO read clock domain.
0: No effect
1: Reset
(R/W)

USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_WR  Configures whether to reset CDC_ACM OUT async FIFO write clock domain.
0: No effect
1: Reset
(R/W)

USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_RD  Configures whether to reset CDC_ACM OUT async FIFO read clock domain.
0: No effect
1: Reset
(R/W)

USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_REMPTY     Represents CDC_ACM OUT async FIFO empty signal in read clock domain. (RO)

USB_SERIAL_JTAG_SERIAL_IN_AFIFO_WFULL       Represents CDC_ACM IN async FIFO full signal in write clock domain. (RO)
```