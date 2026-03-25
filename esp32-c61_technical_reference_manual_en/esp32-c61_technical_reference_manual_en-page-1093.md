

```markdown
Chapter 29 USB Serial/JTAG Controller  
GoBack

Register 29.18. USB_SERIAL_JTAG_JFIFO_ST_REG (0x0020)

| Bit | Description |
|-----|-------------|
| 31-10 | (reserved) |
| 9   | USB_SERIAL_JTAG_OUT_FIFO_RESET |
| 8   | USB_SERIAL_JTAG_IN_FIFO_RESET |
| 7   | USB_SERIAL_JTAG_OUT_FIFO_FULL |
| 6   | USB_SERIAL_JTAG_IN_FIFO_FULL |
| 5   | USB_SERIAL_JTAG_OUT_FIFO_EMPTY |
| 4   | USB_SERIAL_JTAG_IN_FIFO_EMPTY |
| 3   | USB_SERIAL_JTAG_OUT_FIFO_CNT |
| 2   | USB_SERIAL_JTAG_IN_FIFO_CNT |
| 1   | O (Reserved) |
| 0   | Reset |

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