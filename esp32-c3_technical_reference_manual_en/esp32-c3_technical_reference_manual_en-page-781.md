

```markdown
Register 30.13. USB_SERIAL_JTAG_OUT_EPO_ST_REG (0x0038)

| Bit | Description                  |
|-----|------------------------------|
| 31  | reserved                     |
| 30-24| USB_SERIAL_JTAG_OUT_EPO_RD_ADDR |
| 23-16| USB_SERIAL_JTAG_OUT_EPO_WR_ADDR |
| 15-9 | USB_SERIAL_JTAG_OUT_EPO_STATE |
| 8   | Reset                        |

USB_SERIAL_JTAG_OUT_EPO_STATE State of OUT Endpoint 0. (RO)

USB_SERIAL_JTAG_OUT_EPO_WR_ADDR Write data address of OUT Endpoint 0.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected, there are
USB_SERIAL_JTAG_OUT_EPO_WR_ADDR - 2 bytes of data in OUT EPO. (RO)

USB_SERIAL_JTAG_OUT_EPO_RD_ADDR Read data address of OUT endpoint 0. (RO)


Register 30.14. USB_SERIAL_JTAG_OUT_EP1_ST_REG (0x003C)

| Bit | Description                                      |
|-----|--------------------------------------------------|
| 31  | reserved                                         |
| 30-24| USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT             |
| 23-16| USB_SERIAL_JTAG_OUT_EP1_RD_ADDR                  |
| 15-9 | USB_SERIAL_JTAG_OUT_EP1_WR_ADDR                  |
| 8   | USB_SERIAL_JTAG_OUT_EP1_STATE                    |
| 7   | Reset                                            |

USB_SERIAL_JTAG_OUT_EP1_STATE State of OUT Endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_WR_ADDR Write data address of OUT Endpoint 1.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected, there are
USB_SERIAL_JTAG_OUT_EP1_WR_ADDR - 2 bytes of data in OUT EP1. (RO)

USB_SERIAL_JTAG_OUT_EP1_RD_ADDR Read data address of OUT endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT Data count in OUT Endpoint 1 when one packet is
received. (RO)
```