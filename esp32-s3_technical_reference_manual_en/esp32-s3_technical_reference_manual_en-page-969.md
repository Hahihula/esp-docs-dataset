**Title:**
Chapter 26 UART Controller (UART)

**Back Link:**
GoBack

**Register Information:**
- Register Name: UHCI_ESCAPE_CONF_REG (0x0024)
- Bit Positions and Descriptions:
  - **UHCI_TX_CO_ESC_EN**: Set this bit to decode character 0xC0 when DMA receives data. (R/W)
  - **UHCI_TX_DB_ESC_EN**: Set this bit to decode character 0xDB when DMA receives data. (R/W)
  - **UHCI_TX_11_ESC_EN**: Set this bit to decode flow control character 0x11 when DMA receives data.
    - Access Type: Read/Write
  - **UHCI_TX_12_ESC_EN**: Set this bit to decode flow control character 0x13 when DMA receives data. (R/W)
  - **UHCI_RX_CO_ESC_EN**: Set this bit to replace 0xC0 by special characters when DMA sends data.
    - Access Type: Read/Write
  - **UHCI_RX_DB_ESC_EN**: Set this bit to replace 0xDB by special characters when DMA sends data. (R/W)
  - **UHCI_RX_11_ESC_EN**: Set this bit to replace flow control character 0x11 by special characters when DMA sends data.
    - Access Type: Read/Write
  - **UHCI_RX_13_ESC_EN**: Set this bit to replace flow control character 0x13 by special characters when DMA sends data. (R/W)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Link:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback