

```markdown
Register 51.7. USB_SERIAL_JTAG_CHIP_RST_REG (0x004C)

USB_SERIAL_JTAG_RTS Represents the state of RTS signal as set by the most recent SET_LINE_CODING command. (RO)

USB_SERIAL_JTAG_DTR Represents the state of DTR signal as set by the most recent SET_LINE_CODING command. (RO)

USB_SERIAL_JTAG_USB_UART_CHIP_RST_DIS Configures whether to disable chip reset from USB serial channel.
0: No effect
1: Disable
(R/W)
```

```markdown
Register 51.8. USB_SERIAL_JTAG_GET_LINE_CODE_WO_REG (0x0058)

USB_SERIAL_JTAG_GET_DW_DTE_RATE Configures the value of dwDTERate set by software, which is requested by GET_LINE_CODING command. (R/W)
```