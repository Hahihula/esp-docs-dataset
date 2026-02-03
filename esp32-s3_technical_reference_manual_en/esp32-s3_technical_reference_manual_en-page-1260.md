**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Menu:**
GoBack

**Register Information:**
- **Register Name:** USB_SERIAL_JTAG_INT_ST_REG (0x00C)
  
**Diagram Description:**
A binary diagram showing the bit positions for various interrupt statuses.

**Bit Positions and Descriptions in Markdown Format:**

1. **USB_SERIAL_JTAG_IN_FLUSH_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_IN_FLUSH_INT interrupt.
   
2. **USB_SERIAL_JTAG_SOF_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_SOF_INT interrupt.

3. **USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT interrupt.
   
4. **USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT interrupt.

5. **USB_SERIAL_JTAG_PID_ERR_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_PID_ERR_INT interrupt.
   
6. **USB_SERIAL_JTAG_CRC5_ERR_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_CRC5_ERR_INT interrupt.
   
7. **USB_SERIAL_JTAG_CRC16_ERR_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_CRC16_ERR_INT interrupt.

8. **USB_SERIAL_JTAG_STUFF_ERR_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_STUFF_ERR_INT interrupt.
   
9. **USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT_ST**
   - The raw interrupt status bit for the USB_SERIAL_JTAG_IN_TOKEN_REC_IN_EP1_INT interrupt.

10. **USB_SERIAL_JTAG_USB_RESET_INT_ST**
    - The raw interrupt status bit for the USB_SERIAL_JTAG_USB BUS_RESET INT interrupt.
    
11. **USB_SERIAL_JTAG_OUT_EP1_ZERO_PAYLOAD_INT_ST**
    - The raw interrupt status bit for the USB_SERIAL_JTAG_OUT_EP1 ZERO_PAYLOAD INT interrupt.

12. **USB_SERIAL_JTAG_OUT_EP2_ZERO_PAYLOAD_INT_ST**
    - The raw interrupt status bit for the USB_SERIAL_JTAG_OUT_EP2 ZERO_PAYLOAD INT interrupt.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)