**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
GoBack

**Register Information and Description:**

1. **Register 26.23: UART_LOWPULSE_REG (0x0028)**
   - **Field Name:** UART_LOWPULSE_MIN_CNT
   - **Description:** This field stores the value of the minimum duration time of the low level pulse, in the unit of APB_CLK cycles. It is used in baud rate detection.
   - **Access Type:** (RO)
   - **Binary Representation Diagram:**
     ```
     31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
     ```

2. **Register 26.24: UART_HIGHPULSE_REG (0x002C)**
   - **Field Name:** UART_HIGHPULSE_MIN_CNT
   - **Description:** This field stores the value of the maximum duration time for the high level pulse, in the unit of APB_CLK cycles. It is used in baud rate detection.
   - **Access Type:** (RO)
   - **Binary Representation Diagram:**
     ```
     31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
     ```

3. **Register 26.25: UART_RXD_CNT_REG (0x0030)**
   - **Field Name:** UART_RXD_EDGE_CNT
   - **Description:** This field stores the count of RXD edge change. It is used in baud rate detection.
   - **Access Type:** (RO)
   - **Binary Representation Diagram:**
     ```
     31 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
     ```

**Footer Information:**
- Page Number: 963
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Link Texts:**
- Submit Documentation Feedback