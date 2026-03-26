
```markdown
Register 51.16. USB_SERIAL_JTAG_JFIFO_ST_REG (0x0020)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | USB_SERIAL_JTAG_OUT_FIFO_FULL              | Represents whether JTAG OUT FIFO is full.                                  |
| 29  | USB_SERIAL_JTAG_OUT_FIFO_EMPTY             | Represents whether JTAG OUT FIFO is empty.                                 |
| 28  | USB_SERIAL_JTAG_OUT_FIFO_CNT               | Represents JTAG OUT FIFO counter. (RO)                                     |
| 27  | USB_SERIAL_JTAG_IN_FIFO_FULL               | Represents whether JTAG IN FIFO is full.                                   |
| 26  | USB_SERIAL_JTAG_IN_FIFO_EMPTY              | Represents whether JTAG IN FIFO is empty.                                  |
| 25  | USB_SERIAL_JTAG_IN_FIFO_CNT                | Represents JTAG IN FIFO counter. (RO)                                      |
| 24  | USB_SERIAL_JTAG_OUT_FIFO_RESET             | Configures whether to reset JTAG OUT FIFO.                                 |
| 23  | USB_SERIAL_JTAG_IN_FIFO_RESET              | Configures whether to reset JTAG IN FIFO.                                  |

USB_SERIAL_JTAG_IN_FIFO_CNT Represents JTAG IN FIFO counter. (RO)

USB_SERIAL_JTAG_IN_FIFO_EMPTY Represents whether JTAG IN FIFO is empty.
O: Not empty
1: Empty
(RO)

USB_SERIAL_JTAG_IN_FIFO_FULL Represents whether JTAG IN FIFO is full.
O: Not full
1: Full
(RO)

USB_SERIAL_JTAG_OUT_FIFO_CNT Represents JTAG OUT FIFO counter. (RO)

USB_SERIAL_JTAG_OUT_FIFO_EMPTY Represents whether JTAG OUT FIFO is empty.
O: Not empty
1: Empty
(RO)

USB_SERIAL_JTAG_OUT_FIFO_FULL Represents whether JTAG OUT FIFO is full.
O: Not full
1: Full
(RO)

USB_SERIAL_JTAG_IN_FIFO_RESET Configures whether to reset JTAG IN FIFO.
O: No effect
1: Reset
(R/W)

USB_SERIAL_JTAG_OUT_FIFO_RESET Configures whether to reset JTAG OUT FIFO.
O: No effect
1: Reset
(R/W)
```