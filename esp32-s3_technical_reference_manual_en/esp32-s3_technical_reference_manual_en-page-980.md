**Title:**
Chapter 26 UART Controller (UART)

**Header:**
GoBack

**Register Information:**
- Register Name: UHCI_INT_ST_REG (0x0008)
- Binary representation of the register is shown with labels for each bit.

**Bits Description and Functions:**

1. **UHCI_RX_START_INT_ST**: This is the masked interrupt bit for UHCI_RX_START_INT interrupt when UHCI_RX_START_INT_ENA is set to 1.
2. **UHCI_TX_START_INT_ST**: This is the masked interrupt bit for UHCI_TX_START_INT interrupt when UHCI_TX_START_INT_ENA is set to 1.
3. **UHCI_RX_HUNG_INT_ST**: This is the masked interrupt bit for UHCI_RX_HUNG_INT interrupt when UHCI_RX_HUNG_INT_ENA is set to 1 (RO).
4. **UHCI_TX_HUNG_INT_ST**: This is the masked interrupt bit for UHCI_TX_HUNG_INT interrupt when UHCI_TX_HUNG_INT_ENA is set to 1.
5. **UHCI_SEND_S_REG_Q_INT_ST**: This is the masked interrupt bit for UHCI_SEND_S_REG_Q_INT interrupt when UHCI_SEND_S_REG_Q_INT_ENA is set to 1 (RO).
6. **UHCI_SEND_A_REG_Q_INT_ST**: This is the masked interrupt bit for UHCI_SEND_A_REG_Q_INT interrupt when UHCI_SEND_A_REG_Q_INT_ENA is set to 1.
7. **UHCI_OUTLINK_EOF_ERR_INT_ST**: This is the masked interrupt bit for UHCI_OUTLINK_EOF_ERR_INT when UHCI_OUTLINK_EOF_ERR_INT_ENA is set to 1 (RO).
8. **UHCI_APP_CTRL0_INT_ST**: This is the masked interrupt bit for UHCI_APP_CTRL0_INT interrupt when UHCI_APP_CTRL0_INT_ENA is set to 1.
9. **UHCI_APP_CTRL1_INT_ST**: This is the masked interrupt bit for UHCI_APP_CTRL1_INT interrupt when UHCI_APP_CTRL1_INT_ENA is set to 1 (RO).

**Footer:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)

**Link:**
Submit Documentation Feedback