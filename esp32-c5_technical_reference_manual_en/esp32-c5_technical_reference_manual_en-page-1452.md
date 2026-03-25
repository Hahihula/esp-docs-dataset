

```markdown
Chapter 39 SDIO Slave Controller (SDIO)

Figure 39.5-9. Output Timing Diagram

By default, the voltage level of the MTDI strapping pin determines the slave pin's output driving edge. You can also configure the output driving edge using the following registers, with priority from high to low: (1) Set SLCHOST_FRC_SDIO11 in SLCHOST_CONF_REG to output the corresponding signal at the falling clock edge; (2) Set SLCHOST_FRC_SDIO22 in SLCHOST_CONF_REG to output at the rising clock edge; (3) Set HINF_HIGHSPEED_ENABLE in HINF_CFG_DATA1_REG and SLCHOST_HSPEED_CON_EN in SLCHOST_CONF_REG, then set the EHS (Enable High-Speed) bit in CCCR at the host side to output at the rising clock edge.

The SLCHOST_FRC_SDIO11 and SLCHOST_FRC_SDIO22 fields are five bits wide, corresponding to the CMD line and four DATA lines (0–3). Setting a bit causes the corresponding line to output at the rising or falling clock edge.

Note on priority: The configuration of strapping pins has the lowest priority for controlling the sampling or driving edge. Lower-priority configurations take effect only when higher-priority configurations are not set. For example, the GPIO25 strapping value determines the sampling edge only when SCLHOST_FRC_POS_SAMP and SCLHOST_FRC_NEG_SAMP are not set.

39.6 Interrupt

The host and slave can interrupt each other via the interrupt vector. There are eight interrupt vectors between the host and each DMA SLC channel of the slave. To send an interrupt, set the enable bit of the interrupt vector register to 1.

39.6.1 Host Interrupt

*   SLCHOST_SLCO/1_RX_NEW_PACKET_INT: The slave has a packet to send. This interrupt can be triggered when:
    *   SDIO_SLCO_RXLINK_START or SDIO_SLC1_RXLINK_START is set to enable DMA.
    *   A new RX linked list descriptor is available after DMA processes the RX linked list descriptor with the eof bit set to 1.
    *   A packet needs to be retransmitted.
*   SLCHOST_SLCO/1_TX_OVF_INT: Slave TX (transmit) buffer overflow interrupt.
*   SLCHOST_SLCO/1_RX_UDF_INT: Slave RX (receive) buffer underflow interrupt.
*   SLCHOST_SLCO/1_TOHOST_BITn_INT (n: 0–7): Slave interrupts the host.
```