

```markdown
|Bit Name|Description|
|:---------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|31|reserved|
|12|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|11|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|10|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|9|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|8|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|7|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|6|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|5|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|4|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|3|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|2|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|1|USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW|
|0|Reset|

USB_SERIAL_JTAG_JTAG_IN_FLUSH_INT_RAW The raw interrupt bit turns to high level when a flush command is received for IN endpoint 2 of JTAG. (R/WTC/SS)

USB_SERIAL_JTAG_SOF_INT_RAW The raw interrupt bit turns to high level when a SOF frame is received. (R/WTC/SS)

USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT_RAW The raw interrupt bit turns to high level when the Serial Port OUT Endpoint received one packet. (R/WTC/SS)

USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_RAW The raw interrupt bit turns to high level when the Serial Port IN Endpoint is empty. (R/WTC/SS)

USB_SERIAL_JTAG_PID_ERR_INT_RAW The raw interrupt bit turns to high level when a PID error is detected. (R/WTC/SS)

USB_SERIAL_JTAG_CRC5_ERR_INT_RAW The raw interrupt bit turns to high level when a CRC5 error is detected. (R/WTC/SS)

USB_SERIAL_JTAG_CRC16_ERR_INT_RAW The raw interrupt bit turns to high level when a CRC16 error is detected. (R/WTC/SS)

USB_SERIAL_JTAG_STUFF_ERR_INT_RAW The raw interrupt bit turns to high level when a bit stuffing error is detected. (R/WTC/SS)

USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_RAW The raw interrupt bit turns to high level when an IN token for IN endpoint 1 is received. (R/WTC/SS)

USB_SERIAL_JTAG_USB_BUS_RESET_INT_RAW The raw interrupt bit turns to high level when a USB bus reset is detected. (R/WTC/SS)

USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_RAW The raw interrupt bit turns to high level when OUT endpoint 1 received packet with zero payload. (R/WTC/SS)

USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_RAW The raw interrupt bit turns to high level when OUT endpoint 2 received packet with zero payload. (R/WTC/SS)
```