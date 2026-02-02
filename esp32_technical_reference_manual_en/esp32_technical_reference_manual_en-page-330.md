**Title:**
Chapter 19 UART Controller (UART)

**Subtitles and Content with Descriptions of Registers:**

- **Register 19.6. UART_CLKDIV_REG (0x14)**
  - **Field: UART_CLKDIV_FRAG**
    - Description: The decimal part of the frequency divider factor.
    - Access Type: Read/Write
    - Example Value: 0x0002B6

  - **Field: UART_CLKDIV**
    - Description: The integral part of the frequency divider factor.

- **Register 19.7. UART_AUTOBAUD_REG (0x18)**
  - **Field: UART_GLITCH FILT**
    - Description: When the input pulse width is lower than this value, the pulse is ignored.
    - Access Type: Read/Write
    - Example Value: 0x010

  - **Field: UART_AUTOBAUD_EN**
    - Description: This is the enable bit for autobaud.

**Footer Information:**
- Page Number: 330
- Company Name: Espressif Systems
- Document Title: ESP32 TRM (Version 5.6)
- Link Texts:
  - "Submit Documentation Feedback"