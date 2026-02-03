**Title:**
Chapter 33 USB Serial/JTAG Controller (USB_SERIAL_JTAG)

**Link:**
GoBack

**Section Title and Description:**

- **Register 33.4. USB_SERIAL_JTAG_MISC_CONF_REG (0x0044)**
  - **Field:** USB_SERIAL_JTAG_CLK_EN
    - **Description:** 
      - `1'h1`: Force clock on for register.
      - `1'h0`: Support clock only when application writes registers. (R/W)
  
- **Register 33.5. USB_SERIAL_JTAG_MEM_CONF_REG (0x0048)**
  - **Fields:**
    - **USB_SERIAL_JTAG_USB_MEM_PD**: 
      - Description:
        - `1`: power down usb memory. (R/W)
    - **USB_SERIAL_JTAG_USB_MEM_CLK_EN**:
      - Description:
        - `1`: Force clock on for usb memory. (R/W)

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7) 
Submit Documentation Feedback