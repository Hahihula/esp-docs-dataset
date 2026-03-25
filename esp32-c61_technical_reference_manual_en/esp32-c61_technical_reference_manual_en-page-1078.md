

```markdown
Chapter 29 USB Serial/JTAG Controller

Register 29.3. USB_SERIAL_JTAG_CONFO_REG (0x0018)

Continued from the previous page...

USB_SERIAL_JTAG_USB_JTAG_BRIDGE_EN Configures whether to disconnect USB_JTAG and internal JTAG.
O: USB_JTAG is connected to the internal JTAG port of CPU
  1: USB_JTAG and the internal JTAG are disconnected, MTMS, MTDI, and MTCK are output through GPIO Matrix, and MTDO is input through GPIO Matrix (R/W)

USB_SERIAL_JTAG_USB_PHY_TX_EDGE_SEL Configures the clock edge at which DP and DM signals are transmitted to the USB PHY.
O: Transmit on the falling edge of the clock
  1: Transmit on the rising edge of the clock (R/W)
```