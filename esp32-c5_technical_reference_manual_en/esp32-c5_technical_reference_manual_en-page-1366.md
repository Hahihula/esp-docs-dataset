
```markdown
Register 37.16. USB_SERIAL_JTAG_INT_ENA_REG (0x0010)

| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  |                                                                             | Reset                                                                                                                                       |
| 30  |                                                                             | Reset                                                                                                                                       |
| 29  |                                                                             | Reset                                                                                                                                       |
| 28  |                                                                             | Reset                                                                                                                                       |
| 27  |                                                                             | Reset                                                                                                                                       |
| 26  |                                                                             | Reset                                                                                                                                       |
| 25  |                                                                             | Reset                                                                                                                                       |
| 24  |                                                                             | Reset                                                                                                                                       |
| 23  |                                                                             | Reset                                                                                                                                       |
| 22  |                                                                             | Reset                                                                                                                                       |
| 21  |                                                                             | Reset                                                                                                                                       |
| 20  |                                                                             | Reset                                                                                                                                       |
| 19  |                                                                             | Reset                                                                                                                                       |
| 18  |                                                                             | Reset                                                                                                                                       |
| 17  |                                                                             | Reset                                                                                                                                       |
| 16  |                                                                             | Reset                                                                                                                                       |
| 15  | USB_SERIAL_JTAG_SET_LINE_CODE_INT_ENA                                     | Write to enable USB_SERIAL_JTAG_SET_LINE_CODE_INT. (R/W)                                                                                   |
| 14  | USB_SERIAL_JTAG_GET_LINE_CODE_INT_ENA                                     | Write to enable USB_SERIAL_JTAG_GET_LINE_CODE_INT. (R/W)                                                                                  |
| 13  | USB_SERIAL_JTAG_DTR_CHG_INT_ENA                                           | Write to enable USB_SERIAL_JTAG_DTR_CHG_INT. (R/W)                                                                                        |
| 12  | USB_SERIAL_JTAG_RTS_CHG_INT_ENA                                           | Write to enable USB_SERIAL_JTAG_RTS_CHG_INT. (R/W)                                                                                        |
| 11  | USB_SERIAL_JTAG_OUT_CHG_INT_ENA                                          | Write to enable USB_SERIAL_JTAG_OUT_CHG_INT. (R/W)                                                                                        |
| 10  | USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_ENA                             | Write to enable USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT. (R/W)                                                                          |
| 9   | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_ENA                             | Write to enable USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (R/W)                                                                          |
| 8   | USB_SERIAL_JTAG_IN_FLUSH_INT_ENA                                          | Write 1 to enable USB_SERIAL_JTAG_IN_FLUSH_INT. (R/W)                                                                                     |
| 7   | USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_ENA                              | Write 1 to enable USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT. (R/W)                                                                        |
| 6   | USB_SERIAL_JTAG_USB_BUS_RESET_INT_ENA                                     | Write 1 to enable USB_SERIAL_JTAG_USB_BUS_RESET_INT. (R/W)                                                                                |
| 5   | USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_ENA                             | Write 1 to enable USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT. (R/W)                                                                        |
| 4   | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_ENA                             | Write 1 to enable USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (R/W)                                                                        |
| 3   | USB_SERIAL_JTAG_SOF_ERR_INT_ENA                                           | Write 1 to enable USB_SERIAL_JTAG_SOF_ERR_INT. (R/W)                                                                                       |
| 2   | USB_SERIAL_JTAG_STUFF_ERR_INT_ENA                                         | Write 1 to enable USB_SERIAL_JTAG_STUFF_ERR_INT. (R/W)                                                                                    |
| 1   | USB_SERIAL_JTAG_PID_ERR_INT_ENA                                           | Write 1 to enable USB_SERIAL_JTAG_PID_ERR_INT. (R/W)                                                                                       |
| 0   | Reset                                                                      | Reset                                                                                                                                       |

USB_SERIAL_JTAG_IN_FLUSH_INT_ENA Write 1 to enable USB_SERIAL_JTAG_IN_FLUSH_INT. (R/W)

USB_SERIAL_JTAG_SOF_INT_ENA Write 1 to enable USB_SERIAL_JTAG_SOF_INT. (R/W)

USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT_ENA Write 1 to enable USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT. (R/W)

USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_ENA Write 1 to enable USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT. (R/W)

USB_SERIAL_JTAG_PID_ERR_INT_ENA Write 1 to enable USB_SERIAL_JTAG_PID_ERR_INT. (R/W)

USB_SERIAL_JTAG_CRC5_ERR_INT_ENA Write 1 to enable USB_SERIAL_JTAG_CRC5_ERR_INT. (R/W)

USB_SERIAL_JTAG_CRC16_ERR_INT_ENA Write 1 to enable USB_SERIAL_JTAG_CRC16_ERR_INT. (R/W)

USB_SERIAL_JTAG_STUFF_ERR_INT_ENA Write 1 to enable USB_SERIAL_JTAG_STUFF_ERR_INT. (R/W)

USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_ENA Write 1 to enable USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT. (R/W)

USB_SERIAL_JTAG_USB_BUS_RESET_INT_ENA Write 1 to enable USB_SERIAL_JTAG_USB_BUS_RESET_INT. (R/W)

USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_ENA Write 1 to enable USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (R/W)

USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_ENA Write 1 to enable USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT. (R/W)

Continued on the next page...
```