

```markdown
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG) GoBack


Register 33.5. USB_SERIAL_JTAG_MISC_CONF_REG (0x0044)

USB_SERIAL_JTAG_CLK_EN Configures whether to force clock on for register.
- 0: Support clock only when an application writes registers
- 1: Force clock on for register
(R/W)


Register 33.6. USB_SERIAL_JTAG_MEM_CONF_REG (0x0048)

USB_SERIAL_JTAG_USB_MEM_PD Configures whether to power down USB memory.
- 0: No effect
- 1: Power down
(R/W)

USB_SERIAL_JTAG_USB_MEM_CLK_EN Configures whether to force clock on for USB memory.
- 0: No effect
- 1: Force
(R/W)
```