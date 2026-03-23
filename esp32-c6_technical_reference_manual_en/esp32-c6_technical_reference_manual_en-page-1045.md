

```markdown
| Bit | Name                                 | Description                                                                                                                                                                                                 |
|-----|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                                                                                                                                                           |
| 7   | USB_SERIAL_JTAG_TEST_RX_DM          | Represents the logical level of the USB D- pad in test mode. (RO)<br>0: USB D- voltage is higher than USB D+<br>1: USB D+ voltage is higher than USB D- (RO)                                                                 |
| 6   | USB_SERIAL_JTAG_TEST_RX_DP          | Represents the logical level of the USB D+ pad in test mode. (RO)<br>0: USB D- voltage is higher than USB D+<br>1: USB D+ voltage is higher than USB D- (RO)                                                                 |
| 5   | USB_SERIAL_JTAG_TEST_TX_DM          | Configures value of USB D- in test mode when USB_SERIAL_JTAG_TEST_USB_OE is 1. (R/W)<br>0: Set D- to high impedance<br>1: Output the values set in USB_SERIAL_JTAG_TEST_TX_DP and USB_SERIAL_JTAG_TEST_TX_DM on the D+ and D- pins (R/W) |
| 4   | USB_SERIAL_JTAG_TEST_TX_DP          | Configures value of USB D+ in test mode when USB_SERIAL_JTAG_TEST_USB_OE is 1. (R/W)<br>0: Set D+ to high impedance<br>1: Output the values set in USB_SERIAL_JTAG_TEST_RX_DM and USB_SERIAL_JTAG_TEST_RX_DP on the D+ and D- pins (R/W) |
| 3   | USB_SERIAL_JTAG_TEST_USB_OE         | Configures whether to enable USB pad output.<br>0: Set D+ and D- to high impedance<br>1: Output the values set in USB_SERIAL_JTAG_TEST_TX_DP and USB_SERIAL_JTAG_TEST_TX_DM on the D+ and D- pins (R/W) |
| 2   | USB_SERIAL_JTAG_TEST_RX_RCVD        | Represents the current logical level of the voltage difference between USB D- and USB D+ pads in test mode.<br>0: USB D- voltage is higher than USB D+<br>1: USB D+ voltage is higher than USB D- (RO) |
| 1   | USB_SERIAL_JTAG_TEST_USB_ENABLE     | Configures whether to enable the test mode of the USB pad.<br>0: Resume normal operation<br>1: Enable the test mode of the USB pad Enabling the test mode of the USB pad allows the USB pad to be controlled/read using the other bits in this register. (R/W) |
| 0   | Reset                                |                                                                                                                                                                                                           |

Register 32.4. USB_SERIAL_JTAG_TEST_REG (0x001C)
```