**Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Header:**
GoBack

**Register Information:**
- Register Name: RINTSTS_REG (0x0044)
- Bit Positions:
  - 31 to 16 are labeled as "reserved"
  - Bits from 15 down to bit 0 have specific meanings.

**Bit Description Table:**

| Bit | Description |
|-----|-------------|
| **SDIO_INTERRUPT_RAW** | Interrupt from SDIO card, one bit for each card. Bit[17:16] correspond to card1 and card0, respectively. Setting a bit clears the corresponding interrupt bit and writing 0 has no effect. (R/W) |
| - O | No SDIO interrupt from card; |
| - I | SDIO interrupt from card. In MMC-Ver3.3-only mode, these bits are always 0. Bits are logged regardless of interrupt-mask status. (R/W) |
| **INT_STATUS_RAW** | Setting a bit clears the corresponding interrupt and writing 0 has no effect. Bits are logged regardless of interrupt mask status. (R/W) |
| - Bit 15 (EBE) | End-bit error, read/write (no CRC) |
| - Bit 14 (ACD) | Auto command done |
| - Bit 13 (SBE/BCI) | Start Bit Error/Busy Clear Interrupt |
| - Bit 12 (HLE) | Hardware locked write error |
| - Bit 11 (FRUN) | FIFO underrun/overrun error |
| - Bit 10 (HTO) | Data starvation by host timeout (HTO) |
| - Bit 9 (DTRO) | Data read timeout |
| - Bit 8 (RTO) | Response timeout |
| - Bit 7 (DCRC) | Data CRC error |
| - Bit 6 (RCRC) | Response CRC error |
| - Bit 5 (RXDR) | Receive FIFO data request |
| - Bit 4 (TXDR) | Transmit FIFO data request |
| - Bit 3 (DTO) | Data transfer over |
| - Bit 2 (CD) | Command done |
| - Bit 1 (RE) | Response error |
| - Bit 0 (CD) | Card detect |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback