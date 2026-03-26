

```markdown
Chapter 51 USB Serial/JTAG Controller (USB_SERIAL_JTAG)                                     GoBack


Register 51.5. USB_SERIAL_JTAG_MISC_CONF_REG (0x0044)

[Diagram: Register bit field with 32 bits, labeled "(reserved)" for upper bits, and a single bit at position 1 labeled "USB_SERIAL_JTAG_CLK_EN" with value 0 at reset.]

USB_SERIAL_JTAG_CLK_EN   Configures whether to force clock on for register.
    0: Support clock only when application writes registers
    1: Force clock on for register
    (R/W)


Register 51.6. USB_SERIAL_JTAG_MEM_CONF_REG (0x0048)

[Diagram: Register bit field with 32 bits, labeled "(reserved)" for upper bits, and two bits at positions 2 and 1 labeled "USB_SERIAL_JTAG_USB_MEM_CLK_EN" and "USB_SERIAL_JTAG_USB_MEM_PD" respectively, with values 0 at reset.]

USB_SERIAL_JTAG_USB_MEM_PD   Configures whether to power down USB memory.
    0: No effect
    1: Power down
    (R/W)

USB_SERIAL_JTAG_USB_MEM_CLK_EN   Configures whether to force clock on for USB memory.
    0: No effect
    1: Force
    (R/W)
```