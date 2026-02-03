**Title:**
Chapter 26 UART Controller (UART)

**Subtitle:**
Register 26.59. UHCI_INT_RAW_REG (0x0004)

**Body Text with Descriptions of Interrupts and Registers:**

- **UHCI_RX_START_INT_RAW**: This is the interrupt raw bit for UHCI_RX_START_INT. The interrupt is triggered when a separator has been sent.
  - Register Offset/Width: R/WTC/SS

- **UHCI_TX_START_INT_RAW**: This is the interrupt raw bit for UHCI_TX_START_INT. The interrupt is triggered when UHCI detects a separator.

- **UHCI_RX_HUNG_INT_RAW**: This is the interrupt raw bit for UHCI_RX_HUNG_INT. The interrupt triggers are not specified in detail.
  - Register Offset/Width: R/WTC/SS

- **UHCI_TX_HUNG_INT_RAW**: This is the interrupt raw bit for UHCI_TX_HUNG_INT. The interrupt triggers when more time to receive data than configured value.

- **UHCI_SEND_S_REG_Q_INT_RAW**: This is the interrupt raw bit for UHCI_SEND_S_REG_Q. The interrupt trigger details are not specified.
  - Register Offset/Width: R/WTC/SS

- **UHCI_SEND_A_REG_Q_INT_RAW**: This is the interrupt raw bit for UHCI_SEND_A_REG_Q. The interrupt triggers when a short packet using always_send mode.

- **UHCI_OUT_EOF_INT_RAW**: This is the interrupt raw bit for UHCI_OUT_EOF. The interrupt trigger details are not specified.
  - Register Offset/Width: R/WTC/SS

- **UHCI_APP_CTRL0_INT_RAW**: This is the interrupt raw bit for UHCI_APP_CTRL0. The interrupt triggers when UHCI_APP_CTRL0_IN_SET.

- **UHCI_APP_CTRL1_INT_RAW**: This is the interrupt raw bit for UHCI_APP_CTRL1. The interrupt trigger details are not specified.
  - Register Offset/Width: R/W

**Footer Information:**
Espressif Systems
Page Number: 979
Document Version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback