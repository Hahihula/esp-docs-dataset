**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Subtitles and Sections with Descriptions of Registers:**

1. **Register 33.14. USB_SERIAL_JTAG_IN_EP1_ST_REG (0x002C)**
   - Description:
     ```
     0  O    O    O    O    O    O    O    O    O    O
     16 | 15 | 14 | 13 | 12 | 11 | 10 | 9  | 8   | 7  |
         -------------------------------
     ```
   - Fields:
     - `USB_SERIAL_JTAG_IN_EP1_ST_ADDR`: State of IN Endpoint 1. (RO)
     - `USB_SERIAL_JTAG_IN_EP1_WR_ADDR`: Write data address of IN endpoint 1. (RO)
     - `USB_SERIAL_JTAG_IN_EP1_RD_ADDR`: Read data address of IN endpoint 1. (RO)

2. **Register 33.15. USB_SERIAL_JTAG_IN_EP2_ST_REG (0x0030)**
   - Description:
     ```
     0  O    O    O    O    O    O    O    O    O
     16 | 15 | 14 | 13 | 12 | 11 | 10 | 9  | 8   | 7  |
         -------------------------------
     ```
   - Fields:
     - `USB_SERIAL_JTAG_IN_EP2_ST_ADDR`: State of IN Endpoint 2. (RO)
     - `USB_SERIAL_JTAG_IN_EP2_WR_ADDR`: Write data address of IN endpoint 2. (RO)
     - `USB_SERIAL_JTAG_IN_EP2_RD_ADDR`: Read data address of IN endpoint 2. (RO)

**Footer:**
- "Espressif Systems"
- Page number and document version:
  ```
  ESP32-S3 TRM (Version 1.7)
  ```