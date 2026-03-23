

```markdown
Chapter 34 SDIO Slave Controller (SDIO)

GoBack

Notes on priority setting: The configuration of strapping pins has the lowest priority when controlling the sampling edge or driving edge. The lower-priority configuration takes effect only when the higher-priority configuration is not set. For example, the MTMS (GPIO4) strapping value determines the sampling edge only when SCLHOST_FRC_POS_SAMP and SCLHOST_FRC_NEG_SAMP are not set.

34.6 Interrupt

The host and the slave can interrupt each other via the interrupt vector. There are 8 interrupt vectors between the host and each DMA SLC channel of the slave. To send an interrupt to the other side, the enable bit of the interrupt vector register should be set to 1.

34.6.1 Host Interrupt

- SLCHOST_SLCO/1_RX_NEW_PACKET_INT: The slave has a packet to send. Any of the cases below can trigger the interrupt.
    - When SDIO_SLCO_RXLINK_START or SDIO_SLC1_RXLINK_START is set to enable DMA
    - When a new RX linked list descriptor is coming after DMA processes the RX linked list descriptor with the eof bit being 1
    - When a packet needs to be retry

- SLCHOST_SLCO/1_TX_OVF_INT: Slave receiving buffer overflow interrupt.
- SLCHOST_SLCO/1_RX_UDF_INT: Slave sending buffer underflow interrupt.
- SLCHOST_SLCO/1_TOHOST_BITn_INT (n: 0 ~ 7): Slave interrupts the host.

34.6.2 Slave Interrupt

- SLCO/1_RX_DSCR_ERR_INT: Slave sending linked list descriptor error.
- SLCO/1_TX_DSCR_ERR_INT: Slave receiving linked list descriptor error.
- SLCO/1_RX_EOF_INT: Slave sending operation is finished.
- SLCO/1_RX_DONE_INT: A single buffer is sent by the slave.
- SLCO/1_TX_SUC_EOF_INT: Slave receiving operation is finished.
- SLCO/1_TX_DONE_INT: A single buffer is finished during receiving operation.
- SLCO/1_TX_OVF_INT: Slave receiving buffer overflow interrupt.
- SLCO/1_RX_UDF_INT: Slave sending buffer underflow interrupt.
- SLCO/1_TX_START_INT: Slave receiving start interrupt.
- SLCO/1_RX_START_INT: Slave sending start interrupt.
- SLC_FRHOST_BITn_INT (n: 0 ~ 15): The host interrupts the slave via the SLCO channel if interrupt vector Bit[7:0] is set or via the SLC1 channel if interrupt vector Bit[15:8] is set.

Espressif Systems
1118
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```