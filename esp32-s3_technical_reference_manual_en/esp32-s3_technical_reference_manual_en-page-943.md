**Title:**
Chapter 26 UART Controller (UART)

**Body Text:**

- enable UART_RXFIFO_FULL_INT interrupt by setting UART_RXFIFO_FULL_INT_ENA;
- detect UART_TXFIFO_FULL_INT and wait until the RXFIFO is full;
- read data from RXFIFO via UART_RXFIFO_RD_BYTE, and obtain the number of bytes received in RXFIFO via UART_RXFIFO_CNT.

**Footer:**
Espressif Systems
943 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback