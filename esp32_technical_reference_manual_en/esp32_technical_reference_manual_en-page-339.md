**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section Header:**
Register 19.20. UART_AT_CMD_POSTCNT_REG (0x4c)

**Field Description and Values Table for UART_AT_CMD_POSTCNT_REG:**
- **Field Name:** UART_POST_IDLE_NUM
- **Description:** This register is used to configure the duration between the last at_cmd and the next data. When the duration is less than what this register indicates, it will not take the previous data as an at_cmd char.
- **Access Mode:** (R/W)
- **Reset Value:** 0

**Section Header:**
Register 19.21. UART_AT_CMD_GAPTOUT_REG (0x50)

**Field Description and Values Table for UART_AT_CMD_GAPTOUT_REG:**
- **Field Name:** UART_RX_GAP_TOUT
- **Description:** This register is used to configure the interval between the at_cmd chars.
  - When the interval is greater than the value of this register, it will not take the data as continuous at_cmd chars. The register should be configured to more than half of the baud rate.

**Section Header:**
Register 19.22. UART_AT_CMD_CHAR_REG (0x54)

**Field Description and Values Table for UART_AT_CMD_CHAR_REG:**
- **Field Name:** UART_CHAR_NUM
- **Description:** This register is used to configure the number of continuous at_cmd chars received by the receiver.
- **Access Mode:** (R/W)
- **Reset Value:** 0

**Field Description and Values Table for UART_AT_CMD_CHAR_REG:**
- **Field Name:** UART_AT_CMD_CHAR
- **Description:** This register is used to configure the content of an at_cmd char.

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)