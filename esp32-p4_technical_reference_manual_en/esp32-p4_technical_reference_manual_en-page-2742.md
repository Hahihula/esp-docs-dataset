

```markdown
- RXDR: Triggered during read operations from card when FIFO level is greater than Receive-Threshold level
- TXDR: Triggered during write operations to card when FIFO level reaches less than or equal to Transmit-Threshold level.
- DTO: Triggered when data transfer completes
- CMDD: Triggered when a command has been executed
- RE: Triggered when response error occurs
- CD: Triggered when a card is detected
- IDSTS_RI: Triggered when data pointed by a DMA descriptor list have been received
- IDSTS_TI: Triggered when data pointed by a DMA descriptor list have been transmitted
- IDSTS_FBE: Triggered when a fatal bus error occurs and the host is stopped during data transmission or reception. When triggered, the DMA disables all bus access.
- IDSTS_DU: Triggered when a DMA descriptor list is not available because the OWNER bit is 0 (DESO [31] = 0)

The SDHOST_RINTSTS_REG and SDHOST_IDSTS_REG register contains all the bits that might cause an interrupt. The SDHOST_INTMASK_REG and SDHOST_IDINTEN_REG register contains an enable bit for each of the events that can cause an interrupt.

There are three interrupt summary bits in the SDHOST_IDSTS_REG register: the card error interrupt summary bit (bit 5 SDHOST_IDSTS_CES), the normal interrupt summary bit (bit 8 SDHOST_IDSTS_NIS), and the abnormal interrupt summary bit (bit 9 SDHOST_IDSTS_AIS). Interrupts are cleared by writing 1 to the corresponding bit. When all the enabled interrupts within a group are cleared, the corresponding summary bit is also all cleared.

Interrupts are not queued. If another interrupt event occurs before the driver has responded to the previous interrupt, no additional interrupts are generated. For example, the SDHOST_IDSTS_RI indicates that one or more data were transferred to the host buffer.

An interrupt is generated only once for simultaneous multiple events. The driver must scan the SDHOST_RINTSTS_REG and SDHOST_IDSTS_REG register for the interrupt cause.
```

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```