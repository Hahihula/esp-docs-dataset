**Chapter Title:**
Chapter 26 UART Controller (UART)

**GoBack Link:** GoBack

---

**Section Header:**
Register 26.26. UART_POPULSE_REG (0x0070)

**Field Description for UART_POSEGE_MIN_CNT Field in Register 26.26:**
- **Field Name:** UARTPOSEGE_MIN_CNT
- **Description:** This field stores the minimal input clock count between two positive edges. It is used in baud rate detection.
- **Access Type:** (RO)

**Binary Representation of Field:**
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0

---

**Section Header:**
Register 26.27. UART_NEGPULSE_REG (0x0074)

**Field Description for UART_NEGEDGE_MIN_CNT Field in Register 26.27:**
- **Field Name:** UARTNEGEDGE_MIN_CNT
- **Description:** This field stores the minimal input clock count between two negative edges. It is used in baud rate detection.
- **Access Type:** (RO)

**Binary Representation of Field:**
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0

---

**Section Header:**
Register 26.28. UART_AT_CMD_PRECNT_REG (0x0050)

**Field Description for UART_PRE_IDLE_NUM Field in Register 26.28:**
- **Field Name:** UART_PRE_IDLE_NUM
- **Description:** This field is used to configure the idle duration time before the first AT_CMD is received by the receiver, in the unit of bit time (the time it takes to transfer one bit).
- **Access Type:** (R/W)

**Binary Representation of Field:**
0 0 0 0 0 0 0 0 0 0 0 0

---

**Footer Information:**
Espressif Systems
964 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback