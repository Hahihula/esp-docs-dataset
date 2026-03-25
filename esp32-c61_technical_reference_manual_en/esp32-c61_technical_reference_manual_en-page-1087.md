

```markdown
Register 29.15. USB_SERIAL_JTAG_INT_ST_REG (0x000C)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                             |                                                                             |
| 30  | Reset                                |                                                                             |
| 29  | USB_SERIAL_JTAG_SET_LINE_CODE_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_SET_LINE_CODE_INT. (RO)      |
| 28  | USB_SERIAL_JTAG_GET_LINE_CODE_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_GET_LINE_CODE_INT. (RO)      |
| 27  | USB_SERIAL_JTAG_DTR_CHG_INT_ST       | The masked interrupt status of USB_SERIAL_JTAG_DTR_CHG_INT. (RO)            |
| 26  | USB_SERIAL_JTAG_RTS_CHG_INT_ST       | The masked interrupt status of USB_SERIAL_JTAG_RTS_CHG_INT. (RO)            |
| 25  | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (RO) |
| 24  | USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT. (RO) |
| 23  | USB_SERIAL_JTAG_USB_BUS_RESET_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_USB_BUS_RESET_INT. (RO)      |
| 22  | USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_ST | The masked interrupt status of USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT. (RO) |
| 21  | USB_SERIAL_JTAG_STUFF_ERR_INT_ST     | The masked interrupt status of USB_SERIAL_JTAG_STUFF_ERR_INT. (RO)          |
| 20  | USB_SERIAL_JTAG_CRC6_ERR_INT_ST      | The masked interrupt status of USB_SERIAL_JTAG_CRC6_ERR_INT. (RO)           |
| 19  | USB_SERIAL_JTAG_PID_ERR_INT_ST       | The masked interrupt status of USB_SERIAL_JTAG_PID_ERR_INT. (RO)            |
| 18  | USB_SERIAL_JTAG_IN_FLUSH_INT_ST      | The masked interrupt status of USB_SERIAL_JTAG_IN_FLUSH_INT. (RO)           |
| 17  | USB_SERIAL_JTAG_SOF_INT_ST           | The masked interrupt status of USB_SERIAL_JTAG_SOF_INT. (RO)                |
| 16  | USB_SERIAL_JTAG_OUT_RECV_PKT_INT_ST  | The masked interrupt status of USB_SERIAL_JTAG_OUT_RECV_PKT_INT. (RO)       |
| 15  | USB_SERIAL_JTAG_IN_EMPTY_INT_ST      | The masked interrupt status of USB_SERIAL_JTAG_IN_EMPTY_INT. (RO)           |
| 14  | USB_SERIAL_JTAG_CRC16_ERR_INT_ST     | The masked interrupt status of USB_SERIAL_JTAG_CRC16_ERR_INT. (RO)          |

Continued on the next page...
```