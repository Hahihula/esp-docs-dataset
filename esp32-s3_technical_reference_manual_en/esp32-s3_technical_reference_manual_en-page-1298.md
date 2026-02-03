**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Section Header: Register 34.20. SDHOST_CDETECT_REG (0x0050)**

- **Field Name:** SDHOST_CARD_DETECT_N
- **Description:** Value on sdhost_card_detect_n input ports (1 bit per card), read-only bits. 0 represents presence of card. Only NUM_CARDS number of bits are implemented. (RO)
- **Bit Positions:**
  - Bit 31 to Bits [2, 1, 0]: Reserved
- **Reset Value:** 0x0

---

**Section Header: Register 34.21. SDHOST_WRPRT_REG (0x0054)**

- **Field Name:** SDHOST_WRITE_PROTECT
- **Description:** Value on sdhost_card_write_prt input ports (1 bit per card). 1 represents write protection. Only NUM_CARDS number of bits are implemented. (RO)
- **Bit Positions:**
  - Bit 31 to Bits [2, 1, 0]: Reserved
- **Reset Value:** 0x0

---

**Section Header: Register 34.22. SDHOST_TCBCNT_REG (0x005C)**

- **Field Name:** SDHOST_TCBCNT
- **Description:** Number of bytes transferred by CIU unit to card. (RO)
- **Bit Positions:**
  - Bit 31 and Bits [0]: Reserved
- **Reset Value:** 0x0

---

**Section Header: Register 34.23. SDHOST_TBBCNT_REG (0x0060)**

- **Field Name:** SDHOST_TBBCNT
- **Description:** Number of bytes transferred between Host/DMA memory and BIU FIFO.
- **Bit Positions:**
  - Bit 31 to Bits [0]: Reserved
- **Reset Value:** 0x0 (RO)

---

**Footer Information:**
Espressif Systems  
Page number: 1298  
Document version: ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback