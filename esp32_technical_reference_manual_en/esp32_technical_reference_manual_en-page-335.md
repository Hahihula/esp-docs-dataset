**Title:**
Chapter 19 UART Controller (UART)

**Subtitles and Body Texts with Descriptions of Registers:**

- **Register 19.12. UART_HIGHPULSE_REG (0x2C)**
  - **Field Description:** 
    - `UART_HIGHPULSE_MIN_CNT`
      - This register stores the value of the minimum duration of the high level pulse.
      - It is used in baud rate detection process.

- **Register 19.13. UART_RXD_CNT_REG (0x30)**
  - **Field Description:**
    - `UART_RXD_EDGE_CNT`
      - This register stores the count of the RxD edge change.
      - It is used in the baud rate detection process.

**Footer Information:**
- Page number and document version:
  - "Espressif Systems ESP32 TRM (Version 5.6)"
  
- Navigation Links:
  - GoBack
  - Submit Documentation Feedback

**Visual Elements Description:** 
- The image contains two diagrams, each representing a register layout with fields labeled as `UART_HIGHPULSE_MIN_CNT` and `UART_RXD_EDGE_CNT`, respectively.
- Each diagram shows the bit positions (e.g., bits from '31' to '0') for different parts of these registers. There are also indications that some areas in both diagrams have been marked as "(reserved)".

**Note:**
The text is structured with clear headings and descriptions, indicating specific fields within the UART controller's registers related to baud rate detection processes (RO).