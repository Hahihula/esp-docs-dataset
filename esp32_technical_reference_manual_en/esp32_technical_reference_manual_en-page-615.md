**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Section Header:**
Register 27.8. BYTCNT_REG (0x0020)

**Body Text:**
BYTCNT_REG Number of bytes to be transferred, should be an integral multiple of Block Size for block transfers. For data transfers of undefined byte lengths, byte count should be set to 0. When byte count is set to 0, it is the responsibility of host to explicitly send stop/abort command to terminate data transfer. (R/W)

**Section Header:**
Register 27.9. INTMASK_REG (0x0024)

**Diagram Description:**
- The diagram shows a register layout with labels for different bits.
- Bits are labeled as follows:
  - Bit 31
  - Bit 18 to bit 16, labeled "SDIO_INT_MASk"
  - Bit 15 (EBE)
  - Bit 14 (ACD) Auto command done
  - Bit 13 (SBE/BCI): Start Bit Error/Busy Clear Interrupt
  - Bit 12 (HLE): Hardware locked write error
  - Bit 11 (FRUN): FIFO underrun/overrun error
  - Bit 10 (HTO): Data starvation-by-host timeout/Volt_switch_int
  - Bit 9 (DRTO): Data read timeout
  - Bit 8 (RTO): Response timeout
  - Bit 7 (DCRC): Data CRC error
  - Bit 6 (RCRC): Response CRC error
  - Bit 5 (RXDR): Receive FIFO data request
  - Bit 4 (TXDR): Transmit FIFO data request
  - Bit 3 (DTO): Data transfer over
  - Bit 2 (CD): Command done
  - Bit 1 (RE): Response error
  - Bit 0 (CD): Card detect

**Additional Information:**
SDIO interrupt mask, one bit for each card. Bit[17:16] correspond to card[15:0] respectively. When masked, SDIO interrupt detection for that card is disabled. O masks an interrupt, and 1 enables an interrupt.

In MMC-Ver3.0 mode, these bits are always O (R/W)

**List Description of Bits Functions in INT_MASK:**
- Bit 16 (EBE): End-bit error, read/write (no CRC)
- Bit 14 (ACD): Auto command done
- Bit 13 (SBE/BCI): Start Bit Error/Busy Clear Interrupt
- Bit 12 (HLE): Hardware locked write error
- Bit 11 (FRUN): FIFO underrun/overrun error
- Bit 10 (HTO): Data starvation-by-host timeout/Volt_switch_int
- Bit 9 (DRTO): Data read timeout
- Bit 8 (RTO): Response timeout
- Bit 7 (DCRC): Data CRC error
- Bit 6 (RCRC): Response CRC error
- Bit 5 (RXDR): Receive FIFO data request
- Bit 4 (TXDR): Transmit FIFO data request
- Bit 3 (DTO): Data transfer over
- Bit 2 (CD): Command done
- Bit 1 (RE): Response error
- Bit 0 (CD): Card detect

**Footer:**
Espressif Systems  
615 ESP32 TRM (Version 5.6)  

**Navigation Links:**
GoBack, Submit Documentation Feedback