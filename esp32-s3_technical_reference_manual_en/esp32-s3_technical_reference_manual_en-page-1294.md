**Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Link:**
GoBack

**Register Information:**
- **Register Name:** SDHOST_RINTSTS_REG (0x0044)
- Diagram Description:
  - The diagram shows a register layout with the following fields labeled from left to right as follows:

    | Field Number | Label |
    |--------------|-------|
    | 31           | reserved |
    | 18           | SDHOST_INT_STATUS_RAW |
    | 17           | (reserved) |
    | 16           | (reserved) |
    | 15           | (reserved) |
    | 0            | Reset |

**Field Description:**
- **SDHOST_SDIO_INTERRUPT_RAW:** Interrupt from SDIO card, one bit for each card. Bit[17:16] corresponds to card1 and card0, respectively. Setting a bit clears the corresponding interrupt bit and writing O has no effect.
  - (R/W)
  - Values:
    - **0:** No SDIO interrupt from card;
    - **1:** SDIO interrupt from card.

- **SDHOST_INT_STATUS_RAW:** Setting a bit clears the corresponding interrupt, regardless of interrupt mask status. 
  - Bits are logged and writing O has no effect.
  - (R/W)
  - Values:
    - Bit 15: EBE – End-bit error/no CRC error;
    - Bit 14: ACD – Auto command done;
    - Bit 13: SBE/BCI – RX Start Bit Error;
    - Bit 12: HLE – Hardware locked write error;
    - Bit 11: FRUN – FIFO underrun/overrun error;
    - Bit 10: HTO – Data starvation by host timeout (HTO);
    - Bit 9: DTRO – Data read timeout;
    - Bit 8: RTO – Response timeout;
    - Bit 7: DCRC – Data CRC error;
    - Bit 6: RCRC – Response CRC error;
    - Bit 5: RXDR – Receive FIFO data request;
    - Bit 4: TXDR – Transmit FIFO data request;
    - Bit 3: DTO – Data transfer over;
    - Bit 2: CD – Command done;
    - Bit 1: RE – Response error;
    - Bit 0 (CD) – Card detect.

**Footer Information:**
- **Company:** Espressif Systems
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 1294

**Link for Feedback:**
Submit Documentation Feedback