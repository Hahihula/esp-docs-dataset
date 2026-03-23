
```markdown
Register 32.12. USB_SERIAL_JTAG_INT_RAW_REG (0x0008)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             | Reset                                                                       |
| 30  |                                             | (reserved)                                                                  |
| 29  | USB_SERIAL_JTAG_SET_LINE_CODE_INT_RAW      |                                                                             |
| 28  | USB_SERIAL_JTAG_GET_DTR_CHG_INT_RAW        |                                                                             |
| 27  | USB_SERIAL_JTAG_RTS_CHG_INT_RAW            |                                                                             |
| 26  | USB_SERIAL_JTAG_OUT_THRU_INT_RAW           |                                                                             |
| 25  | USB_SERIAL_JTAG_OUT_ZERO_EP0_INT_RAW       |                                                                             |
| 24  | USB_SERIAL_JTAG_USB_BUS_INT_RAW            |                                                                             |
| 23  | USB_SERIAL_JTAG_STUFF_ERR_REC_IN_EP1_INT_RAW |                                                                             |
| 22  | USB_SERIAL_JTAG_CRC5_ERR_INT_RAW           |                                                                             |
| 21  | USB_SERIAL_JTAG_PID_ERR_INT_RAW            |                                                                             |
| 20  | USB_SERIAL_JTAG_OUT_RECV_PKTD_INT_RAW      |                                                                             |
| 19  | USB_SERIAL_JTAG_OUT_RECV_PKT_INT_RAW       |                                                                             |
| 18  | USB_SERIAL_JTAG_IN_FLUSH_INT_RAW           | The raw interrupt status of USB_SERIAL_JTAG_IN_FLUSH_INT. (R/WTC/SS)        |
| 17  | USB_SERIAL_JTAG_SOF_INT_RAW                | The raw interrupt status of USB_SERIAL_JTAG_SOF_INT. (R/WTC/SS)             |
| 16  | USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKTD_INT_RAW | The raw interrupt status of USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKTD_INT. (R/WTC/SS)|
| 15  | USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT_RAW | The raw interrupt status of USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT. (R/WTC/SS)|
| 14  | USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_RAW    | The raw interrupt status of USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT. (R/WTC/SS) |
| 13  | USB_SERIAL_JTAG_PID_ERR_INT_RAW            | The raw interrupt status of USB_SERIAL_JTAG_PID_ERR_INT. (R/WTC/SS)         |
| 12  | USB_SERIAL_JTAG_CRC5_ERR_INT_RAW           | The raw interrupt status of USB_SERIAL_JTAG_CRC5_ERR_INT. (R/WTC/SS)        |
| 11  | USB_SERIAL_JTAG_CRC16_ERR_INT_RAW          | The raw interrupt status of USB_SERIAL_JTAG_CRC16_ERR_INT. (R/WTC/SS)       |
| 10  | USB_SERIAL_JTAG_STUFF_ERR_INT_RAW          | The raw interrupt status of USB_SERIAL_JTAG_STUFF_ERR_INT. (R/WTC/SS)       |
| 9   | USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_RAW | The raw interrupt status of USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT. (R/WTC/SS)|
| 8   | USB_SERIAL_JTAG_USB_BUS_RESET_INT_RAW      | The raw interrupt status of USB_SERIAL_JTAG_USB_BUS_RESET_INT. (R/WTC/SS)   |
| 7   | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_RAW | The raw interrupt status of USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (R/WTC/SS)|

Continued on the next page...
```