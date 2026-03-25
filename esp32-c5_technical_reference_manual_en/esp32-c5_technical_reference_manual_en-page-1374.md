

```markdown
## Register 37.25. USB_SERIAL_JTAG_OUT_EP1_ST_REG (0x003C)

| Bit | Description |
|-----|-------------|
| 31-24 | reserved |
| 23   | 0           |
| 22   | 0           |
| 21   | 0           |
| 20   | 0           |
| 19   | 0           |
| 18   | 0           |
| 17   | 0           |
| 16-9 | reserved    |
| 8    | 0           |
| 7    | 0           |
| 6    | 0           |
| 5    | 0           |
| 4    | 0           |
| 3    | 0           |
| 2    | 0           |
| 1    | 0           |
| 0    | Reset       |

USB_SERIAL_JTAG_OUT_EP1_STATE Represents state of OUT Endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_WR_ADDR Represents write data address of OUT endpoint 1.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected, there are
(USB_SERIAL_JTAG_OUT_EP1_WR_ADDR – 2) bytes data in OUT endpoint 1.
(RO)

USB_SERIAL_JTAG_OUT_EP1_RD_ADDR Represents read data address of OUT endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT Represents data count in OUT endpoint 1 when one packet is received. (RO)


## Register 37.26. USB_SERIAL_JTAG_OUT_EP2_ST_REG (0x0040)

| Bit | Description |
|-----|-------------|
| 31-24 | reserved |
| 23   | 0           |
| 22   | 0           |
| 21   | 0           |
| 20   | 0           |
| 19   | 0           |
| 18   | 0           |
| 17   | 0           |
| 16-9 | reserved    |
| 8    | 0           |
| 7    | 0           |
| 6    | 0           |
| 5    | 0           |
| 4    | 0           |
| 3    | 0           |
| 2    | 0           |
| 1    | 0           |
| 0    | Reset       |

USB_SERIAL_JTAG_OUT_EP2_STATE Represents state of OUT Endpoint 2. (RO)

USB_SERIAL_JTAG_OUT_EP2_WR_ADDR Represents write data address of OUT endpoint 2.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected there are
(USB_SERIAL_JTAG_OUT_EP2_WR_ADDR – 2) bytes data in OUT endpoint 2.
(RO)

USB_SERIAL_JTAG_OUT_EP2_RD_ADDR Represents read data address of OUT endpoint 2. (RO)
```