**Title: Chapter 27 SD/MMC Host Controller (SDHOST)**

---

### Register Descriptions:

- **Register 2714. RESP2_REG (0x0038)**
  - **RESP2_REG Bit[95:64] of long response. (RO)**
    - Reset value is `0x000000000`

- **Register 2715. RESP3_REG (0x003C)**
  - **RESP3_REG Bit[127:96] of long response. (RO)**
    - Reset value is `0x000000000`

- **Register 2716. MINTSTS_REG (0x0040)**
  - **SDIO_INTERRUPT_MSK Interrupt from SDIO card, one bit for each card. Bit[17:16] correspond to card1 and card0, respectively. SDIO interrupt for card is enabled only if corresponding sdio_int_mask bit is set in Interrupt mask register (Setting mask bit enables interrupt). (RO)**
    - Reset value is `0x0000000`

  - **INT_STATUS_MSK Interrupt enabled only if corresponding bit in interrupt mask register is set. (RO)**
    - Bit definitions:
      - Bit 15 (EBE): End-bit error, read/write (no CRC)
      - Bit 14 (ACD): Auto command done
      - Bit 13 (SBE/BCI): Start Bit Error/Busy Clear Interrupt
      - Bit 12 (HLE): Hardware locked write error
      - Bit 11 (FRUN): FIFO underrun/overrun error
      - Bit 10 (HTO): Data starvation by host timeout (HTO)
      - Bit 9 (DTRO): Data read timeout
      - Bit 8 (RTO): Response timeout
      - Bit 7 (DCRC): Data CRC error
      - Bit 6 (RCRC): Response CRC error
      - Bit 5 (RXDR): Receive FIFO data request
      - Bit 4 (TXDR): Transmit FIFO data request
      - Bit 3 (DTO): Data transfer over
      - Bit 2 (CD): Command done
      - Bit 1 (RE): Response error
      - Bit 0 (CD): Card detect

---

**Footer:**
- Espresso Systems, ESP32 TRM (Version 5.6)
- Submit Documentation Feedback