

```markdown
|31|7|6|5|4|3|2|1|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|
|0|0|0|0|0|0|0|0|Reset|
```

**USB_SERIAL_JTAG_TEST_ENABLE** Configures whether to enable the test mode of the USB pad.
- 0: Resume normal operation
- 1: Enable the test mode of the USB pad

Enabling the test mode of the USB pad allows the USB pad to be controlled/read using the other bits in this register. (R/W)

---

**USB_SERIAL_JTAG_TEST_USB_OE** Configures whether to enable USB pad output.
- 0: Set D+ and D- to high impedance
- 1: Output the values set in **USB_SERIAL_JTAG_TEST_TX_DP** and **USB_SERIAL_JTAG_TEST_TX_DM** on the D+ and D- pins (R/W)

---

**USB_SERIAL_JTAG_TEST_TX_DP** Configures value of USB D+ in test mode when **USB_SERIAL_JTAG_TEST_USB_OE** is 1. (R/W)

---

**USB_SERIAL_JTAG_TEST_TX_DM** Configures value of USB D- in test mode when **USB_SERIAL_JTAG_TEST_USB_OE** is 1. (R/W)

---

**USB_SERIAL_JTAG_TEST_RX_RCV** Represents the current logical level of the voltage difference between USB D- and USB D+ pads in test mode.
- 0: USB D- voltage is higher than USB D+
- 1: USB D+ voltage is higher than USB D- (RO)

---

**USB_SERIAL_JTAG_TEST_RX_DP** Represents the logical level of the USB D+ pad in test mode. (RO)

---

**USB_SERIAL_JTAG_TEST_RX_DM** Represents the logical level of the USB D- pad in test mode. (RO)
```