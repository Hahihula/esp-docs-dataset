

```markdown
Register 32.15. USB_SERIAL_JTAG_INT_CLR_REG (0x0014)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | Reset                                                                       |
| 31  |                                            | (reserved)                                                                  |
| 30  | USB_SERIAL_JTAG_SET_LINE_CODE_INT_CLR     |                                                                             |
| 29  | USB_SERIAL_JTAG_GET_LINE_CODE_INT_CLR     |                                                                             |
| 28  | USB_SERIAL_JTAG_DTR_CHG_INT_CLR            |                                                                             |
| 27  | USB_SERIAL_JTAG_RTS_CHG_INT_CLR            |                                                                             |
| 26  | USB_SERIAL_JTAG_OUT_EP_INT_CLR             |                                                                             |
| 25  | USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_CLR |                                                                             |
| 24  | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_CLR |                                                                             |
| 23  | USB_SERIAL_JTAG_STUFF_ERR_INT_CLR          | Write 1 to clear USB_SERIAL_JTAG_STUFF_ERR_INT. (WT)                       |
| 22  | USB_SERIAL_JTAG_CRC5_ERR_INT_CLR           | Write 1 to clear USB_SERIAL_JTAG_CRC5_ERR_INT. (WT)                        |
| 21  | USB_SERIAL_JTAG_CRC16_ERR_INT_CLR          | Write 1 to clear USB_SERIAL_JTAG_CRC16_ERR_INT. (WT)                       |
| 20  | USB_SERIAL_JTAG_SOF_INT_CLR                | Write 1 to clear USB_SERIAL_JTAG_SOF_INT. (WT)                             |
| 19  | USB_SERIAL_JTAG_IN_FLUSH_INT_CLR           | Write 1 to clear USB_SERIAL_JTAG_IN_FLUSH_INT. (WT)                        |
| 18  | USB_SERIAL_JTAG_OUT_RECV_PKT_INT_CLR       | Write 1 to clear USB_SERIAL_JTAG_OUT_RECV_PKT_INT. (WT)                    |
| 17  | USB_SERIAL_JTAG_IN_EMPTY_INT_CLR           | Write 1 to clear USB_SERIAL_JTAG_IN_EMPTY_INT. (WT)                        |
| 16  | USB_SERIAL_JTAG_PID_ERR_INT_CLR            | Write 1 to clear USB_SERIAL_JTAG_PID_ERR_INT. (WT)                         |

USB_SERIAL_JTAG_IN_FLUSH_INT_CLR   Write 1 to clear USB_SERIAL_JTAG_IN_FLUSH_INT.
(WT)

USB_SERIAL_JTAG_SOF_INT_CLR        Write 1 to clear USB_SERIAL_JTAG_SOF_INT. (WT)

USB_SERIAL_JTAG_OUT_RECV_PKT_INT_CLR Write 1 to clear
USB_SERIAL_JTAG_OUT_RECV_PKT_INT. (WT)

USB_SERIAL_JTAG_IN_EMPTY_INT_CLR   Write 1 to clear
USB_SERIAL_JTAG_IN_EMPTY_INT. (WT)

USB_SERIAL_JTAG_PID_ERR_INT_CLR    Write 1 to clear USB_SERIAL_JTAG_PID_ERR_INT.
(WT)

USB_SERIAL_JTAG_CRC5_ERR_INT_CLR   Write 1 to clear USB_SERIAL_JTAG_CRC5_ERR_INT.
(WT)

USB_SERIAL_JTAG_CRC16_ERR_INT_CLR  Write 1 to clear USB_SERIAL_JTAG_CRC16_ERR_INT.
(WT)

USB_SERIAL_JTAG_STUFF_ERR_INT_CLR  Write 1 to clear USB_SERIAL_JTAG_STUFF_ERR_INT.
(WT)

USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_CLR Write 1 to clear
USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT. (WT)

USB_SERIAL_JTAG_USB_BUS_RESET_INT_CLR Write 1 to clear USB_SERIAL_JTAG_USB_BUS_RESET_INT.
(WT)

USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_CLR Write 1 to clear
USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT. (WT)

USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_CLR Write 1 to clear
USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT. (WT)
```
Continued on the next page...
```