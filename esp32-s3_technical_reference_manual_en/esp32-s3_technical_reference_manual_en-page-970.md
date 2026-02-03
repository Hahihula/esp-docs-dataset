**Chapter Title:**
Chapter 26 UART Controller (UART)

**Register Information Section Header:**

- **Register Name:** Register 26.37, UHCI_HUNG_CONF_REG (0x0028)
- **Field Description Table:**
  - Field Name: UHCI_TXFIFO_TIMEOUT
    - Description: This field stores the timeout value.
    - Additional Info: UHCI will produce the UHCI_TX_HUNG_INT interrupt when DMA takes more time to receive data. (R/W)
  - Field Name: UHCI_TXFIFO_TIMEOUT_SHIFT
    - Description: This field is used to configure the maximum tick count. (R/W)
  - Field Name: UHCI_TXFIFO_TIMEOUT_ENA
    - Description: This is the enable bit for TX FIFO receive timeout. (R/W)
  - Field Name: UHCI_RXFIFO_TIMEOUT
    - Description: This field stores the timeout value.
    - Additional Info: UHCI will produce the UHCI_RX_HUNG_INT interrupt when DMA takes more time to read data from RAM. (R/W)
  - Field Name: UHCI_RXFIFO_TIMEOUT_SHIFT
    - Description: This field is used to configure the maximum tick count. (R/W)
  - Field Name: UHCI_RXFIFO_TIMEOUT_ENA
    - Description: This is the enable bit for DMA send timeout. (R/W)

- **Register Name:** Register 26.38, UHCI_ACK_NUM_REG (0x002C)
- **Field Description Table:**
  - Field Name: UHCI_ACK_NUM
    - Description: This is the ACK number used in software flow control. (R/W)
  - Field Name: UHCI_ACK_NUM_LOAD
    - Description: Set this bit to 1, and the value configured by UHCI_ACK_NUM would be loaded. (WT)

**Footer Information:**
- Page Number: 970
- Document Version: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback