**Title:**
Chapter 19 UART Controller (UART)

**Header:**
Register 19.33. UHCI_INT_CLR_REG (0x10) - GoBack

**Body Text with List of Interrupts and Their Clearing Instructions:**

- **UHCI_SEND_A_REG_Q_INT_CLR**: Set this bit to clear the UHCI_SEND_A_REG_Q_INT interrupt.
- **UHCI_SEND_S_REG_Q_INT_CLR**: Set this bit to clear the UHCI_SEND_S_REG_Q_INT interrupt.
- **UHCI_OUT_TOTAL_EOF_INT_CLR**: Set this bit to clear the UHCI_OUT_TOTAL_EOF_INT interrupt.
- **UHCI_OUTLINK_EOF_ERR_INT_CLR**: Set this bit to clear the UHCI_OUTLINK_EOF_ERR_INT interrupt. (WO)
- **UHCI_IN_DSCR_EMPTY_INT_CLR**: Set this bit to clear the UHCI_IN_DSCR_EMPTY_INT interrupt.

Continuing in a similar format for other interrupts:

- **UHCI_OUT_DSCR_ERR_INT_CLR**
- **UHCI_OUT_DSCR_ERR_INT_CLR**
- **UHCI_OUT_EOF_INT_CLR**
- **UHCI_OUT_DONE_INT_CLR**
- **UHCI_IN_ERR_EOF_INT_CLR**
- **UHCI_IN_SUC_EOF_INT_CLR**
- **UHCI_IN_DONE_INT_CLR**
- **UHCITX_HUNG_INT_CLR**
- **UHCIRX_HUNG_INT_CLR**
- **UHCITX_START_INT_CLR**
- **UHCIRX_START_INT_CLR**

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
347 ESP32 TRM (Version 5.6)