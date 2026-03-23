

```markdown
Register 30.5. USB_SERIAL_JTAG_MEM_CONF_REG (0x0048)

USB_SERIAL_JTAG_USB_MEM_PD    Set to power down USB memory. (R/W)
USB_SERIAL_JTAG_USB_MEM_CLK_EN   Set to force clock-on for USB memory. (R/W)

Register 30.6. USB_SERIAL_JTAG_EP1_CONF_REG (0x0004)

USB_SERIAL_JTAG_WR_DONE   Set this bit to indicate writing byte data to UART Tx FIFO is done.
This bit then stays 0 until data in UART Tx FIFO is read by the USB Host. (WT)

USB_SERIAL_JTAG_SERIAL_IN_EP_DATA_FREE   1'b1: Indicate UART Tx FIFO is not full and data can be written into in. After writing USB_SERIAL_JTAG_WR_DONE, this will be 1'b0 until the data is sent to the USB Host. (RO)

USB_SERIAL_JTAG_SERIAL_OUT_EP_DATA_AVAIL   1'b1: Indicate there is data in UART Rx FIFO. (RO)
```