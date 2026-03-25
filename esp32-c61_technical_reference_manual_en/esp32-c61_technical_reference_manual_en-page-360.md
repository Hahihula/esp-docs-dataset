

```markdown
Chapter 7 Reset and Clock

Register 7.31. PCR_USB_DEVICE_CONF_REG (0x0080)

PCR_USB_DEVICE_CLK_EN Configures whether or not to enable USB Serial/JTAG clock.
O: Not enable
1: Enable
(R/W)

PCR_USB_DEVICE_RST_EN Configures whether or not to reset USB Serial/JTAG.
O: Not reset
1: Reset
(R/W)

PCR_USB_DEVICE_READY Represents whether or not USB Serial/JTAG is released from reset.
O: Not released
1: Released
(RO)
```