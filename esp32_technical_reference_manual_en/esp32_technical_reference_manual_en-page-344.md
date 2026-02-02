**Title:**
Chapter 19 UART Controller (UART)

**Subtitle:**
Register 19.31, UHCI_INT_ST_REG (0x8)

**Body Text with Descriptions of Register Bits and Interrupts:**

- **UHCI_SEND_A_REG_Q_INT_ST:** The masked interrupt status bit for the UHCI_SEND_A_REG_Q_INT interrupt.
  
- **UHCI_SEND_S_REG_Q_INT_ST:** The masked interrupt status bit for the UHCI_SEND_S_REG_Q_INT interrupt.

- **UHCI_OUT_TOTAL_EOF_INT_ST:** The masked interrupt status bit for the UHCI_OUT_TOTAL_EOF_INT interrupt.

- **UHCI_OUTLINK_EOF_ERR_INT_ST:** The masked interrupt status bit for the UHCI_OUTLINK_EOF_ERR_INT interrupt (RO).

- **UHCI_IN_DSCR_EMPTY_INST:** The masked interrupt status bit for the UHCI_IN_DSCR_EMPTY_INST interrupt. 

- **UHCI_OUT_DSCR_ERR_INT_ST:** The masked interrupt status bit for the UHCI_OUT_DSCR_ERR_INT interrupt.

- **UHCI_IN_DSCR_ERR_INT_ST:** The masked interrupt status bit for the UHCI_IN_DSCR_ERR_INT interrupt (RO).

- **UHCI_OUT_EOF_INT_ST:** The masked interrupt status bit for the UHCI_OUT_EOF_INT interrupt. 

- **UHCI_OUT_DONE_INT_ST:** The masked interrupt status bit for the UHCI_OUTDone_INT interrupt.

- **UHCI_IN_ERR_EOF_INT_ST:** The masked interrupt status bit for the UHCI_INErr_EOF_INT interrupt (RO).

- **UHCI_IN_SUC_EOF_INT_ST:** The masked interrupt status bit for the UHCI_INsuc_EOF_INT interrupt. 

- **UHCI_IN_DONE_INT_ST:** The masked interrupt status bit for the UHCI_INDone_INT interrupt.

- **UHCI_TX_HUNG_INT_ST:** The masked interrupt status bit for the UHCI_TXHung_INT interrupt (RO).

- **UHCI_RX_HUNG_INT_ST:** The masked interrupt status bit for the UHCI_RXHung_INT interrupt. 

**Footer:**
Continued on the next page...

**Page Information at Bottom of Page:**
Espressif Systems
344 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Diagram Description in Image:**

The image contains a bit map diagram showing various bits and their corresponding labels, such as "reserved," UHCI_DMA, INFIFO_FULL, WM, etc., with specific numbers indicating the positions of each label on the register.

(Note: The exact layout details are not transcribed due to complexity.)