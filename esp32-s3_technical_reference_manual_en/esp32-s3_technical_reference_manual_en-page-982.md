**Title:**
Chapter 26 UART Controller (UART)

**Subtitle:**
Register 26.62. UHCI_INT_CLR_REG (0x0010)

**Body Text with List and Descriptions:**

- **UHCI_RX_START_INT_CLR**: Set this bit to clear UHCI_RX_START_INT interrupt.
- **UHCI_TX_START_INT_CLR**: Set this bit to clear UHCI_TX_START_INT interrupt.
- **UHCI_RX_HUNG_INT_CLR**: Set this bit to clear UHCI_RX_HUNG_INT interrupt.
- **UHCI_TX_HUNG_INT_CLR**: Set this bit to clear UHCI_TX_HUNG_INT interrupt.
- **UHCI_SEND_S_REG_Q_INT_CLR**: Set this bit to clear UHCI_SEND_S_REG_Q_INT interrupt.
- **UHCI_SEND_A_REG_Q_INT_CLR**: Set this bit to clear UHCI_SEND_A_REG_Q_INT interrupt.
- **UHCI_OUTLINK_EOF_ERR_INT_CLR**: Set this bit to clear UHCI_OUTLINK_EOF_ERR_INT interrupt.

**Register 26.63:**
UHCI_APP_INT_SET_REG (0x0014)

- **UHCI_APP_CTRL0_INT_SET**: This bit is software interrupt trigger source of UHCI_APP_CTRL0_INT.
- **UHCI_APP_CTRL1_INT_SET**: This bit is software interrupt trigger source of UHCI_APP_CTRL1_INT.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
982 ESP32-S3 TRM (Version 1.7)