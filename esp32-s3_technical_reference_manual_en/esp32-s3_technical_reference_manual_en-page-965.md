**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Titles and Descriptions with Registers Information:**

1. **Register 26.29. UART_AT_CMD_POSTCNT_REG (0x0054)**
   - Description:
     - `UART_POST_IDLE_NUM`: This field is used to configure the duration time between the last AT_CMD and the next data byte, in the unit of bit time (the time it takes to transfer one bit). (R/W)
   - Binary Representation: 31 0 O O O O

2. **Register 26.30. UART_AT_CMD_GAPOUT_REG (0x0058)**
   - Description:
     - `UART_RX_GAP_TOUT`: This field is used to configure the duration time between the AT_CMD characters, in the unit of bit time (the time it takes to transfer one bit). (R/W)
   - Binary Representation: 31 0 O O O

3. **Register 26.31. UART_AT_CMD_CHAR_REG (0x005C)**
   - Description:
     - `UART_AT_CMD_CHAR`: This field is used to configure the content of AT_CMD character. (R/W)
       - `UART_CHAR_NUM`: This field is used to configure the number of continuous AT_CMD characters received by the receiver. (R/W)
   - Binary Representation: 31 0 O

**Footer Information:**
- Page Number and Document Version:
  - "965 ESP32-S3 TRM (Version 1.7)"
- Company Name:
  - Espressif Systems
- Action Links:
  - Submit Documentation Feedback