

```markdown
- `RECV_WDT_TO`: Triggered when `DMAIN_RWTE` is 1 and the Receive Watchdog Timer has expired while receiving the current frame.
- `EARLY_TRANS_INT`: Triggered when `DMAIN_ETIE` is 1 and the frame has been completely transmitted to MTL TX FIFO.
- `FATAL_BUS_ERR_INT`: Triggered when `DMAIN_FBEE` is 1 and a bus error described in `ERROR_BITS` occurs.

• `NORM_INT_SUMM`: Triggered when `DMAIN_NISE` is 1 and the following interrupts are triggered.
    - `TRANS_INT`: Triggered when `DMAIN_TIE` is 1 and the transmission completes.
    - `TRANS_BUF_UNAVAILABLE`: Triggered when `DMAIN_TBUE` is 1, the Host owns the Next Descriptor in the Transmit List and the DMA cannot acquire it.
    - `RECV_INT`: Triggered when `DMAIN_RIE` is 1 and the frame has been received.
    - `EARLY_RECV_INT`: Triggered when `DMAIN_ERIE` is 1 and the DMA has received the first buffer of the data packet.

**EMAC_PMT_INT**: Triggered when `PMTINTMASK` is 0, and a magic packet or a remote wakeup frame has been received in power-down mode.

**TS_TRI_INT**: Triggered when `TSINTMASK` is 0 and any of the following conditions is true:
    - The system time value equals or exceeds the value specified in the Target Time registers
    - There is an overflow in the System Time Seconds Register

**EMAC_LPI_INT**: Triggered when `LPIINTMASK` is 0 and any of the following conditions is true:
    - The MAC Transmitter enters the LPI state
    - The MAC Transmitter exits the LPI state
    - The MAC Receiver enters the LPI state
    - The MAC Receiver exits the LPI state

The following interrupt sources can generate the `PMT_INTR` interrupt signal:

• `RWKPRCVD`: Triggered when a remove wakeup frame is received.
• `MGKPRCVD`: Triggered when a magic packet is received.

The following interrupt source can generate the `LPI_INTR` interrupt signal:

• `RLPIEX`: Triggered when the MAC receiver has stopped receiving the LPI pattern on PHY and has exited the LPI state.
```