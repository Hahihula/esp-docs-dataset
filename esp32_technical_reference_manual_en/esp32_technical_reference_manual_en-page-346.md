**Title:**
Chapter 19 UART Controller (UART)

**Header:**
Register 19.32. UHCI_INT_ENA_REG (0xC)

**Menu/Navigation Link:**
GoBack

**Table Description and Labels for Interrupt Enable Bits in the Register:**

- **UHCI_SEND_A_REG_Q_INT_ENA**: The interrupt enable bit for the `UHCI_SEND_A_REG_Q_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_SEND_S_REG_Q_INT_ENA**: The interrupt enable bit for the `UHCI_SEND_S_REG_Q_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_OUT_TOTAL_EOF_INT_ENA**: The interrupt enable bit for the `UHCI_OUT_TOTAL_EOF_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_OUTLINK_EOF_ERR_INT_ENA**: The interrupt enable bit for the `UHCI_OUTLINK_EOF_ERR_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_IN_DSCR_EMPTY_INT_ENA**: The interrupt enable bit for the `UHCI_IN_DSCR_EMPTY_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_OUT_DSCR_ERR_INT_ENA**: The interrupt enable bit for the `UHCI_OUT_DSCR_ERR_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_IN_DSCR_ERR_INT_ENA**: The interrupt enable bit for the `UHCI_IN_DSCR_ERR_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_OUT_EOF_INT_ENA**: The interrupt enable bit for the `UHCI_OUT_EOF_INT` interrupt, which is a part of the `UHCI_OUT_EOC_INT` interrupt line. 
  - Access Mode: Read/Write (R/W)
  
- **UHCI_OUT_DONE_INT_ENA**: The interrupt enable bit for the `UHCI_OUTDone_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_IN_ERR_EOF_INT_ENA**: The interrupt enable bit for the `UHCI_INErr_EOF_INT` interrupt, which is a part of the `UHCI_INErr_INT` line. 
  - Access Mode: Read/Write (R/W)
  
- **UHCI_INSuc_EOF_INT_ENA**: The interrupt enable bit for the `UHCI_INSuc_EOF_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_inDone_INT_ENA**: The interrupt enable bit for the `UHCI_inDone_INT` interrupt, which is a part of the `UHCI_in_INT` line. 
  - Access Mode: Read/Write (R/W)
  
- **UHCI_TX_HUNG_INT_ENA**: The interrupt enable bit for the `UHCI_TXHung_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_RX_HUNG_INT_ENA**: The interrupt enable bit for the `UHCI_RXHung_INT` interrupt, which is a part of the `UHCI_RXHung_INT` line. 
  - Access Mode: Read/Write (R/W)
  
- **UHCI_TX_START_INT_ENA**: The interrupt enable bit for the `UHCI_TXStart_INT` interrupt.
  - Access Mode: Read/Write (R/W)
  
- **UHCI_RX_START_INT_ENA**: The interrupt enable bit for the `UHCI_RXStart_INT` interrupt, which is a part of the `UHCI_RXStart_INT` line. 
  - Access Mode: Read/Write (R/W)

**Footer Information:**
Espressif Systems
Page Number: 346
Document Version: ESP32 TRM (Version 5.6)
Link Texts:
- Submit Documentation Feedback