

```markdown
Register 37.12. USB_SERIAL_JTAG_SERIAL_EP_TIMEOUT0_REG (0x006C)

USB_SERIAL_JTAG_SERIAL_TIMEOUT_EN USB serial out endpoint timeout enable. When a timeout event occurs, serial out endpoint buffer is automatically cleared and USB_SERIAL_JTAG_SERIAL_TIMEOUT_STATUSis asserted.

0: timeout disabled, buffer will not be cleared automatically
1: timeout enabled
(R/W)

USB_SERIAL_JTAG_SERIAL_TIMEOUT_STATUS Timeout status bit
0: No timeout occurred.
1: Serial out endpoint has triggered a timeout event.
(R/WTC/SS)

USB_SERIAL_JTAG_SERIAL_TIMEOUT_STATUS_CLR Write 1 to clear USB_SERIAL_JTAG_SERIAL_TIMEOUT_STATUS. (WT)

Register 37.13. USB_SERIAL_JTAG_SERIAL_EP_TIMEOUT1_REG (0x0070)

USB_SERIAL_JTAG_SERIAL_TIMEOUT_MAX USB serial out endpoint timeout max threshold value, indicates the maximum time that waiting for chips to take away data in memory. This value is in steps of 20.83 ns. (R/W)
```