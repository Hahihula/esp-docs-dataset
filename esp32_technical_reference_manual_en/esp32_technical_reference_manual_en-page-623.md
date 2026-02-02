**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Register Section:**

- **Register Name and Address:**
  - Register 27.20, CDETECT_REG (0x0050)
    - Description:
      ```
      CARD_DETECT_N Value on card_detect_n input ports (1 bit per card), read-only bits.0 represents presence of card. Only NUM_CARDS number of bits are implemented. (RO)
      ```

- **Register Name and Address:**
  - Register 27.21, WRTPRT_REG (0x0054)
    - Description:
      ```
      WRITE_PROTECT Value on card_write_prt input ports (1 bit per card).1 represents write protection. Only NUM_CARDS number of bits are implemented. (RO)
      ```

- **Register Name and Address:**
  - Register 27.22, TCBCNT_REG (0x005C)
    - Description:
      ```
      TCBCNT_REG Number of bytes transferred by CIU unit to card. (RO)
      ```

- **Register Name and Address:**
  - Register 27.23, TBBCNT_REG (0x0060)
    - Description:
      ```
      TBBCNT_REG Number of bytes transferred between Host/DMA memory and BIU FIFO. (RO)
      ```

---

**Footer Information:** 
- Page number: 623
- Company name: Espressif Systems
- Document version: ESP32 TRM (Version 5.6)

**Feedback Link:** Submit Documentation Feedback