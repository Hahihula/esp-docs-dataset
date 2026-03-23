
```markdown
| Chapter 30 USB Serial/JTAG Controller (USB_SERIAL_JTAG) | GoBack |
|---|---|
| **Register 30.19. USB_SERIAL_JTAG_INT_CLR_REG (0x0014)** |  |

| Bit | Description |
|-----|-------------|
| 31 | reserved |
| 30-12 | reserved |
| 11 | USB_SERIAL_JTAG_IN_FLUSH_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_IN_FLUSH_INT interrupt. (WT) |
| 10 | USB_SERIAL_JTAG_SOF_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_SOF_INT interrupt. (WT) |
| 9 | USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT interrupt. (WT) |
| 8 | USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT interrupt. (WT) |
| 7 | USB_SERIAL_JTAG_PID_ERR_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_PID_ERR_INT interrupt. (WT) |
| 6 | USB_SERIAL_JTAG_CRC5_ERR_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_CRC5_ERR_INT interrupt. (WT) |
| 5 | USB_SERIAL_JTAG_CRC16_ERR_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_CRC16_ERR_INT interrupt. (WT) |
| 4 | USB_SERIAL_JTAG_STUFF_ERR_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_STUFF_ERR_INT interrupt. (WT) |
| 3 | USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_IN_TOKEN_IN_EP1_INT interrupt. (WT) |
| 2 | USB_SERIAL_JTAG_USB_BUS_RESET_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_USB_BUS_RESET_INT interrupt. (WT) |
| 1 | USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT interrupt. (WT) |
| 0 | USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_CLR<br/>Set this bit to clear the USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT interrupt. (WT) |
```