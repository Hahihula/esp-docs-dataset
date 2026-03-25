
```markdown
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

Register 33.21. USB_SERIAL_JTAG_IN_EP3_ST_REG (0x0034)


| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-9      | (reserved)                                 |                                                                             |
| 8         | USB_SERIAL_JTAG_IN_EP3_RD_ADDR             | Represents read data address of IN endpoint 3. (RO)                          |
| 7-2       | USB_SERIAL_JTAG_IN_EP3_WR_ADDR             | Represents write data address of IN endpoint 3. (RO)                         |
| 1-0       | USB_SERIAL_JTAG_IN_EP3_STATE               | Represents state of IN endpoint 3. (RO)                                     |

USB_SERIAL_JTAG_IN_EP3_STATE    Represents state of IN endpoint 3. (RO)
USB_SERIAL_JTAG_IN_EP3_WR_ADDR   Represents write data address of IN endpoint 3. (RO)
USB_SERIAL_JTAG_IN_EP3_RD_ADDR   Represents read data address of IN endpoint 3. (RO)

Register 33.22. USB_SERIAL_JTAG_OUT_EPO_ST_REG (0x0038)


| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-9      | (reserved)                                 |                                                                             |
| 8         | USB_SERIAL_JTAG_OUT_EPO_RD_ADDR            | Represents read data address of OUT endpoint 0. (RO)                         |
| 7-2       | USB_SERIAL_JTAG_OUT_EPO_WR_ADDR            | Represents write data address of OUT endpoint 0.                            |
| 1-0       | USB_SERIAL_JTAG_OUT_EPO_STATE              | Represents state of OUT endpoint 0. (RO)                                    |

USB_SERIAL_JTAG_OUT_EPO_STATE    Represents state of OUT endpoint 0. (RO)
USB_SERIAL_JTAG_OUT_EPO_WR_ADDR   Represents write data address of OUT endpoint 0.
When     USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT      is detected, there are
(USB_SERIAL_JTAG_OUT_EPO_WR_ADDR – 2) bytes data in OUT endpoint 0.
(RO)

USB_SERIAL_JTAG_OUT_EPO_RD_ADDR   Represents read data address of OUT endpoint 0. (RO)
```