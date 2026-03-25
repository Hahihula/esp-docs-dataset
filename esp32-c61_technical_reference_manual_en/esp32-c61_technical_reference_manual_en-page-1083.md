

```markdown
| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                  | -                                                                                                                                           |
| 6   | USB_SERIAL_JTAG_SERIAL_IN_AFIFO_WFFULL                                    | Represents CDC_ACM IN async FIFO full signal in write clock domain. (RO)                                                                   |
| 5   | USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_REMPTY                                   | Represents CDC_ACM OUT async FIFO empty signal in read clock domain. (RO)                                                                  |
| 4   | USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_RD                                 | Configures whether to reset CDC_ACM OUT async FIFO read clock domain.<br>0: No effect<br>1: Reset (R/W) |
| 3   | USB_SERIAL_JTAG_SERIAL_OUT_AFIFO_RESET_WR                                | Configures whether to reset CDC_ACM OUT async FIFO write clock domain.<br>0: No effect<br>1: Reset (R/W) |
| 2   | USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_WR                                 | Configures whether to reset CDC_ACM IN async FIFO write clock domain.<br>0: No effect<br>1: Reset (R/W) |
| 1   | USB_SERIAL_JTAG_SERIAL_IN_AFIFO_RESET_RD                                 | Configures whether to reset CDC_ACM IN async FIFO read clock domain.<br>0: No effect<br>1: Reset (R/W) |
| 0   | Reset                                                                      | -                                                                                                                                           |

Register 29.11. USB_SERIAL_JTAG_SER_AFIFO_CONFIG_REG (0x0064)
```