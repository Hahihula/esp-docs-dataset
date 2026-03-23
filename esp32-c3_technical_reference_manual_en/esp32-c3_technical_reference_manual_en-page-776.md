

```markdown
Chapter 30 USB Serial/JTAG Controller (USB_SERIAL_JTAG)
GoBack

Register 30.3. USB_SERIAL_JTAG_TEST_REG (0x001C)

[Diagram: Bitfield for USB_SERIAL_JTAG_TEST_REG]
31 | Reset
   | 4 | 3 | 2 | 1 | 0
   |---|---|---|---|---|
   | 0 | 0 | 0 | 0 | 0 | 0

USB_SERIAL_JTAG_TEST_ENABLE Enable test of the USB pad. (R/W)
USB_SERIAL_JTAG_TEST_USB_OE USB pad output enable in test. (R/W)
USB_SERIAL_JTAG_TEST_TX_DP USB D+ tx value in test. (R/W)
USB_SERIAL_JTAG_TEST_TX_DM USB D- tx value in test. (R/W)

Register 30.4. USB_SERIAL_JTAG_MISC_CONF_REG (0x0044)

[Diagram: Bitfield for USB_SERIAL_JTAG_MISC_CONF_REG]
31 | Reset
   | 1
   |---|
   | 0

USB_SERIAL_JTAG_CLK_EN 1'h1: Force clock on for register. 1'h0: Support clock only when application writes registers. (R/W)
```