

```markdown
Register 54.26. SDHOST_INTMASK_REG (0x0024)

SDHOST_INT_MASK Write 1 to correspond bit to enable correspond interrupt. For every bit:
Bit 15 (EBE): End-bit error/no CRC error
Bit 14 (ACD): Auto command done
Bit 13 (SBE/BCI): Rx Start Bit Error
Bit 12 (HLE): Hardware locked write error
Bit 11 (FRUN): FIFO overrun/overrun error
Bit 10 (HTO): Data starvation-by-host timeout
Bit 9 (DRT0): Data read timeout
Bit 8 (RTO): Response timeout
Bit 7 (DCRC): Data CRC error
Bit 6 (RCRC): Response CRC error
Bit 5 (RXDR): Receive FIFO data request
Bit 4 (TXDR): Transmit FIFO data request
Bit 3 (DTO): Data transfer over
Bit 2 (CMDD): Command done
Bit 1 (RE): Response error
Bit 0 (CD): Card detect
(R/W)

SDHOST_SDIO_INT_MASK Write 1 to correspond bit to enable interrupt from correspond card. One bit per card. Bit[0] corresponds to card[0]. (R/W)
```