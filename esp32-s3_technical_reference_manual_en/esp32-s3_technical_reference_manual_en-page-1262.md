**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Subtitle:**
Register 33.9. USB_SERIAL_JTAG_INT_CLR_REG (0x0014)

**Body Text with Descriptions of Register Bits and Their Functions:**

- **USB_SERIAL_JTAG_IN_FLUSH_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_JTAG_IN_FLUSH_INT interrupt.
  
- **USB_SERIAL_JTAG_SOF_IN_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_JTAG_SOF_IN_interrupt.

- **USB_SERIAL_JTAG SERIAL_OUT_RECV_PKT_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT interrupt.
  
- **USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT interrupt.

- **USB_SERIAL_JTAG_PID_ERR_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_PID_ERR_INT interrupt.

- **USB_SERIAL_JTAG_CRC5_ERR_INT_CLR**
  - Description: This bit is used for clearing the USB_SERIAL_JTAG_CRC5_ERR_INT interrupt.
  
- **USB_SERIAL_JTAG_CRC16_ERR_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_CRC16_ERR_INT interrupt.

- **USB_SERIAL_JTAG_STUFF_ERR_INT_CLR**
  - Description: This bit is used for clearing the USB_SERIAL_JTAG_STUFF_ERR_INT interrupt.
  
- **USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT interrupt.

- **USB_SERIAL_JTAG_USB BUS_RESET_INT_CLR**
  - Description: This register is used for clearing the USB_SERIAL_JTAG_USB BUS_RESET_INT interrupt.
  
- **USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_CLR**
  - Description: Set this bit to clear the USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT interrupt.

- **USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_CLR**
  - Description: This register is used for clearing the USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT interrupt.
  
**Footer Information:**

- Page Number: 1262
- Document Version: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Additional Elements in Image:**
- A binary representation of the register is shown with labels for each bit.
- The label "Reset" indicates that setting certain bits to '0' will clear specific interrupts.

**Navigation Link:**
- GoBack (link or button)