**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Register Information Section**

- **Register Name and Address:**
  - Register 34.15, SDHOST_RESP3_REG (0x003c)
    - Bit[127:96] of long response.
    - (RO)

- **Register Name and Address:**
  - Register 34.16, SDHOST_MINTSTS_REG (0x0040)
    - Reserved

**Diagram Description:** 
- A diagram showing the relationship between registers:
  - `SDHOST_SDIO_INT_STATUS_MSK`
  - `SDHOST_SDIO_INT_MSTK`

---

**Interrupt Mask Register:**
- **Register Name and Address:**
  - SDHOST_SDIO_INTERRUPT_MSK
    - Interrupt from SDIO card, one bit for each card.
    - Bit[17:16] corresponds to card1 and card0 respectively. SDIO interrupt for card is enabled only if corresponding `SDHOST_sdio_int_mask` bit in the Interrupt mask register (Setting mask bit enables interrupt).
    - (RO)

**Interrupt Status Mask Register:**
- **Register Name and Address:**
  - SDHOST_INT_STATUS_MSK
    - Interrupt enabled only if a corresponding bit in the interrupt mask register is set.
    - Bit definitions:
      - Bit 15, EBE: End-bit error/no CRC error;
      - Bit 14, ACD: Auto command done;
      - Bit 13, SBE/BCI: RX Start Bit Error;
      - Bit 12, HLE: Hardware locked write error;
      - Bit 11, FRUN: FIFO underrun/overrun error;
      - Bit 10, HTO: Data starvation by host timeout (HTO);
      - Bit 9, DTRO: Data read timeout;
      - Bit 8, RTO: Response timeout;
      - Bit 7, DCRC: Data CRC error;
      - Bit 6, RCRC: Response CRC error;
      - Bit 5, RXDR: Receive FIFO data request;
      - Bit 4, TXDR: Transmit FIFO data request;
      - Bit 3, DTO: Data transfer over;
      - Bit 2, CD: Command done;
      - Bit 1, RE: Response error;
      - Bit 0, CD: Card detect.

---

**Footer Information:** 
- Espressif Systems
- Document Version and Link:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback