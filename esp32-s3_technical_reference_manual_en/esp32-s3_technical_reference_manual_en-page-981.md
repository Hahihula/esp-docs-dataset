**Title:**
Chapter 26 UART Controller (UART)

**Header:**
Register 26.61, UHCI_INT_ENA_REG (0x00C0)

**Diagram Description:**
- A binary register diagram with labels for each bit position from right to left.
- Bits are labeled as follows:
  - Bit positions range from 'Reset' on the far right through various interrupt enable bits such as "UHCI_RX_START_INT_ENA", etc., up to an unspecified label at the end.

**Body Text:**
1. **UHCI_RX_START_INT_ENA**: This is the interrupt enable bit for UHCI_RX_START_INT interrupt.
2. **UHCI_TX_START_INT_ENA**: This is the interrupt enable bit for UHCI_TX_START_INT interrupt (R/W).
3. **UHCI_RX_HUNG_INT_ENA**: This is the interrupt enable bit for UHCI_RX_HUNG_INT interrupt.

4. **UHCI_TX_HUNG_INT_ENA**: This is the interrupt enable bit for UHCI_TX_HUNG_INT interrupt.
5. **UHCI_SEND_S_REG_Q_INT_ENA**: This is the interrupt enable bit for UHCI_SEND_S_REG_Q_INT interrupt (R/W).
6. **UHCI_SEND_A_REG_Q_INT_ENA**: This is the interrupt enable bit for UHCI_SEND_A_REG_Q_INT interrupt.

7. **UHCI_OUTLINK_EOF_ERR_INT_ENA**: This is the interrupt enable bit for UHCI_OUTLINK_EOF_ERR_INT interrupt.
8. **UHCI_APP_CTRL0_INT_ENA**: This is the interrupt enable bit for UHCI_APP_CTRL0_INT interrupt (R/W).
9. **UHCI_APP_CTRL1_INT_ENA**: This is the interrupt enable bit for UHCI_APP_CTRL1_INT interrupt.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)