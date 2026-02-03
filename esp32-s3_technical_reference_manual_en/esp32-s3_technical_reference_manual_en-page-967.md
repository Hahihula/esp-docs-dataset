**Chapter Title:**
Chapter 26 UART Controller (UART)

**Register Information:**
- Register Name: UHCI_CONFO_REG (0x0000)
- Description of bits:
  - **UHCI_TX_RST**: Write 1, the write O to this bit to reset decode state machine. (R/W)
  - **UHCI_RX_RST**: Write 1, the write O to this bit to reset encode state machine. (R/W)
  - **UHCI_UARTO_CE**: Set this bit to link up UHCI and UART0. (R/W)
  - **UHCI_UART1_CE**: Set this bit to link up UHCI and UART1. (R/W)
  - **UHCI_UART2_CE**: Set this bit to link up UHCI and UART2. (R/W)
  - **UHCI_SEPER_EN**: Set this bit to separate the data frame using a special character. (R/W)
  - **UHCI_HEAD_EN**: Set this bit to encode the data packet with a formatting header. (R/W)
  - **UHCI_CRC_REC_EN**: Set this bit to enable UHCI to receive the 16 bit CRC. (R/W)
  - **UHCI_UART_IDLE_EOF_EN**: If this bit is set to 1, UHCI will end the payload receiving process when UART has been in idle state. (R/W)
  - **UHCI_LEN_EOF_EN**: If this bit is set to 1, UHCI decoder stops receiving payload data when the number of received data bytes has reached the specified value. The value is payload length indicated by UHCI packet header when UHCI_HEAD_EN is 1 or the value is configuration value when UHCI_HEAD_EN is O. If this bit is set to 0, UHCI decoder stops receiving payload data when 0xCO has been received. (R/W)
  - **UHCI_ENCODE_CRC_EN**: Set this bit to enable data integrity check by appending a 16 bit CCITT-CRC to end of the payload. (R/W)
  - **UHCI_CLK_EN_0**: Support clock only when application writes registers; 1: Force clock on for registers. (R/W)
  - **UHCI_UART_RX_BRK_EOF_EN**: If this bit is set to 1, UHCI will end payload receive process when NULL frame is received by UART. (R/W)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 967

**Navigation Links:**
- Submit Documentation Feedback