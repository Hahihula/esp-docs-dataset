

```markdown
Register 51.21. USB_SERIAL_JTAG_IN_EP3_ST_REG (0x0034)

USB_SERIAL_JTAG_IN_EP3_STATE    Represents state of IN Endpoint 3. (RO)
USB_SERIAL_JTAG_IN_EP3_WR_ADDR   Represents write data address of IN endpoint 3. (RO)
USB_SERIAL_JTAG_IN_EP3_RD_ADDR   Represents read data address of IN endpoint 3. (RO)

Register 51.22. USB_SERIAL_JTAG_OUT_EPO_ST_REG (0x0038)

USB_SERIAL_JTAG_OUT_EPO_STATE    Represents state of OUT Endpoint O. (RO)
USB_SERIAL_JTAG_OUT_EPO_WR_ADDR   Represents write data address of OUT endpoint O.
When     USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT      is detected, there are
(USB_SERIAL_JTAG_OUT_EPO_WR_ADDR – 2) bytes data in OUT endpoint O.
(RO)

USB_SERIAL_JTAG_OUT_EPO_RD_ADDR    Represents read data address of OUT endpoint O. (RO)
```