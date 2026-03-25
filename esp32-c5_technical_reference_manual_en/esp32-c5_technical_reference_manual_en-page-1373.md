

```markdown
Chapter 37 USB Serial/JTAG Controller

Register 37.23. USB_SERIAL_JTAG_IN_EP3_ST_REG (0x0034)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-16     | reserved                                   |                                                                             |
| 15        | USB_SERIAL_JTAG_IN_EP3_STATE               | Represents state of IN Endpoint 3. (RO)                                    |
| 9         | USB_SERIAL_JTAG_IN_EP3_WR_ADDR             | Represents write data address of IN endpoint 3. (RO)                        |
| 8         | USB_SERIAL_JTAG_IN_EP3_RD_ADDR             | Represents read data address of IN endpoint 3. (RO)                         |

Register 37.24. USB_SERIAL_JTAG_OUT_EPO_ST_REG (0x0038)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-16     | reserved                                   |                                                                             |
| 15        | USB_SERIAL_JTAG_OUT_EPO_STATE              | Represents state of OUT Endpoint O. (RO)                                    |
| 9         | USB_SERIAL_JTAG_OUT_EPO_WR_ADDR            | Represents write data address of OUT endpoint O.                           |
| 8         | USB_SERIAL_JTAG_OUT_EPO_RD_ADDR            | Represents read data address of OUT endpoint O. (RO)                        |

When `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` is detected, there are `(USB_SERIAL_JTAG_OUT_EPO_WR_ADDR - 2)` bytes data in OUT endpoint O. (RO)
```