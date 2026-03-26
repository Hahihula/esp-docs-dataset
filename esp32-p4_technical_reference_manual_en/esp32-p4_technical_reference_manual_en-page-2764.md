

```markdown
Register 54.27. SDHOST_MINTSTS_REG (0x0040)

SDHOST_INT_STATUS_MSK The masked interrupt status. For every bit:
Bit 15 (EBE): End-bit error/no CRC error
Bit 14 (ACD): Auto command done
Bit 13 (SBE/BCI): RX Start Bit Error
Bit 12 (HLE): Hardware locked write error
Bit 11 (FRUN): FIFO underrun/overrun error
Bit 10 (HTO): Data starvation by host timeout
Bit 9 (DTRO): Data read timeout
Bit 8 (RTO): Response timeout
Bit 7 (DCRC): Data CRC error
Bit 6 (RCRC): Response CRC error
Bit 5 (RXDR): Receive FIFO data request
Bit 4 (TXDR): Transmit FIFO data request
Bit 3 (DTO): Data transfer over
Bit 2 (CMDD): Command done
Bit 1 (RE): Response error
Bit 0 (CD): Card detect (RO)

SDHOST_SDIO_INTERRUPT_MSK The masked interrupt status from SDIO card. One bit for each card. Bit[0] corresponds to card[0]. (RO)
```