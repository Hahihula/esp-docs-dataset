

```markdown
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)
GoBack

Register 33.23. USB_SERIAL_JTAG_OUT_EP1_ST_REG (0x003C)

| 31 | 23 | 22 | ... | 16 | 15 | 9 | 8 | 2 | 1 | 0 |
|-----|-----|-----|------|----|----|---|---|---|---|---|
| 0   | 0   | 0   | 0    | 0  |     | 0 | 0 | 0 | 0 | Reset |

USB_SERIAL_JTAG_OUT_EP1_STATE Represents state of OUT endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_WR_ADDR Represents write data address of OUT endpoint 1.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected, there are
(USB_SERIAL_JTAG_OUT_EP1_WR_ADDR – 2) bytes data in OUT endpoint 1.
(RO)

USB_SERIAL_JTAG_OUT_EP1_RD_ADDR Represents read data address of OUT endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT Represents data count in OUT endpoint 1 when one
packet is received. (RO)

Register 33.24. USB_SERIAL_JTAG_OUT_EP2_ST_REG (0x0040)

| 31 | 16 | 15 | ... | 9 | 8 | 2 | 1 | 0 |
|-----|-----|----|------|---|---|---|---|---|
| 0   | 0   | 0  | 0    | 0 |     | 0 | 0 | Reset |

USB_SERIAL_JTAG_OUT_EP2_STATE Represents state of OUT endpoint 2. (RO)

USB_SERIAL_JTAG_OUT_EP2_WR_ADDR Represents write data address of OUT endpoint 2.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected there are
(USB_SERIAL_JTAG_OUT_EP2_WR_ADDR – 2) bytes data in OUT endpoint 2.
(RO)

USB_SERIAL_JTAG_OUT_EP2_RD_ADDR Represents read data address of OUT endpoint 2. (RO)
```