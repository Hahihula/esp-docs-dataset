**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Subtitles and Content:**

1. **Register 33.16, USB_SERIAL_JTAG_IN_EP3_ST_REG (0x0034)**
   - Description:
     ```
     0  O  O  O  O  O  O  O  O  O
     15 | 14 | 13 | 12 | 11 | 10 |
     ---------------------------
     USB_SERIAL_JTAG_IN_EP3_RO_ADDR (reserved)
     ```
   - Fields:
     - `USB_SERIAL_JTAG_IN_EP3_STATE`: State of IN Endpoint 3. (RO)

2. **Register 33.16, USB_SERIAL_JTAG_IN_EP3_WR_ADDR**
   - Description: Write data address of IN endpoint 3. (RO)
   - Fields:

3. **Register 33.16, USB_SERIAL_JTAG_IN_EP3_RD_ADDR**
   - Description: Read data address of IN endpoint 3. (RO)

4. **Register 33.17, USB_SERIAL_JTAG_OUT_EPO_ST_REG (0x0038)**
   - Description:
     ```
     0  O  O  O  O  O  O  O  O  O
     15 | 14 | 13 | 12 | 11 | 10 |
     ---------------------------
     USB_SERIAL_JTAG_OUT_EPO_WR_ADDR (reserved)
     ```
   - Fields:
     - `USB_SERIAL_JTAG_OUT_EPO_STATE`: State of OUT Endpoint O. (RO)

5. **Register 33.17, USB_SERIAL_JTAG_OUT_EPO_WR_ADDR**
   - Description: Write data address of OUT endpoint O.
   - Fields:

6. **Register 33.17, USB_SERIAL_JTAG_OUT_EPO_RD_ADDR-2 bytes in OUT EPO. (RO)**
   - When `USB_SERIAL_JTAG_SERIAL_USB_OUT_RECV_PKT_INT` is detected:
     - Description: Read data address of OUT endpoint O.

**Footer Information:**
- Page number: 1266
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback