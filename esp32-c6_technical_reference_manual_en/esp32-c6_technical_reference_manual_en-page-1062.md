

```markdown
## Register 32.23. USB_SERIAL_JTAG_OUT_EP1_ST_REG (0x003C)

| Bit 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|        |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | USB_SERIAL_JTAG_OUT_EP1_WR_ADDR | USB_SERIAL_JTAG_OUT_EP1_RD_ADDR | USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT | USB_SERIAL_JTAG_OUT_EP1_STATE |

USB_SERIAL_JTAG_OUT_EP1_STATE Represents state of OUT Endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_WR_ADDR Represents write data address of OUT endpoint 1.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected, there are
(USB_SERIAL_JTAG_OUT_EP1_WR_ADDR – 2) bytes data in OUT endpoint 1.
(RO)

USB_SERIAL_JTAG_OUT_EP1_RD_ADDR Represents read data address of OUT endpoint 1. (RO)

USB_SERIAL_JTAG_OUT_EP1_REC_DATA_CNT Represents data count in OUT endpoint 1 when one packet is received. (RO)


## Register 32.24. USB_SERIAL_JTAG_OUT_EP2_ST_REG (0x0040)

| Bit 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----| (reserved) | USB_SERIAL_JTAG_OUT_EP2_RD_ADDR | USB_SERIAL_JTAG_OUT_EP2_WR_ADDR | USB_SERIAL_JTAG_OUT_EP2_STATE |

USB_SERIAL_JTAG_OUT_EP2_STATE Represents state of OUT Endpoint 2. (RO)

USB_SERIAL_JTAG_OUT_EP2_WR_ADDR Represents write data address of OUT endpoint 2.
When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is detected there are
(USB_SERIAL_JTAG_OUT_EP2_WR_ADDR – 2) bytes data in OUT endpoint 2.
(RO)

USB_SERIAL_JTAG_OUT_EP2_RD_ADDR Represents read data address of OUT endpoint 2. (RO)
```