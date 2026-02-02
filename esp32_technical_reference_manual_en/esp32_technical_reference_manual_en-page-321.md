**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section Titles and Content:**

1. **FIFO data pop register**
   - UHCI_DMA_IN_POP_REG

2. **DMA status**
   - UHCI_DMA_OUT_STATUS_REG:
     - Description: DMA FIFO status.
   - UHCI_DMA_OUT_EOF_DES_ADDR_REG, UHCI_DMA_OUT_EOF_BFR_DES_ADDR_REG, UHCI_DMA_IN_SUC_EOF_DESC_ADDR_REG,
     - Description: Out EOF link descriptor address on success. Out EOF link descriptor address on error.

3. **Interrupt registers**
   - UHCI_INT_RAW_REG:
     - Description: Raw interrupt status.
   - UHCI_INT_ST_REG:
     - Description: Masked interrupt status.
   - UHCI_INT_ENA_REG, UHCI_INT_CLR_REG,
     - Description: Interrupt enable bits and Interrupt clear bits.

**Table Entries (with address ranges in hexadecimal):**

- **FIFO data pop register**
  - Address Range: 0x3FF54020 to 0x3FF4C020
  - Access Type: RO

- **DMA status**
  - UHCI_DMA_OUT_STATUS_REG:
    - Address: 0x3FF54014, Read Only (RO)
  - Out EOF link descriptor address on success.
  
- **Interrupt registers**
  - Raw interrupt status:
    - Address Range: 0x3FF54004 to 0x3FF4C004
    - Access Type: RO
  
**Footer Information:**

- Company Name: Espressif Systems
- Document Version and Page Number: ESP32 TRM (Version 5.6), page number not specified.
- Link Texts:
  - "Submit Documentation Feedback"