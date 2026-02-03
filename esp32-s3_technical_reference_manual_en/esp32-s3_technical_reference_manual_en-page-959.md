**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.13. UART_SWFC_CONFO_REG (0x003C)

**Field Descriptions and Values in Register 26.13:**

- **UART_XOFF_THRESHOLD:** When the number of data bytes in RX FIFO is more than the value of this field with UART_SW_FLOWCON_EN set to 1, the transmitter sends an XOFF character.
- **UART_XOFF_CHAR:** This field stores the XOFF flow control character.

**Section Header:**
Register 26.14. UART_SWFC_CONF1_REG (0x0040)

**Field Descriptions and Values in Register 26.14:**

- **UART_XON_THRESHOLD:** When the number of data bytes in RX FIFO is less than the value of this field with UART_SW_FLOWCON_EN set to 1, the transmitter sends an XON character.
- **UART_XON_CHAR:** This field stores the XON flow control character.

**Section Header:**
Register 26.15. UART_TXBRK_CONF_REG (0x0044)

**Field Descriptions and Values in Register 26.15:**

- **UART_TX_BRK_NUM:** This field is used to configure the number of 0s to be sent after the process of sending data is done. It is active when UART_TXD_BRK is set to 1.

**Footer Information:**
Espressif Systems
959 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback