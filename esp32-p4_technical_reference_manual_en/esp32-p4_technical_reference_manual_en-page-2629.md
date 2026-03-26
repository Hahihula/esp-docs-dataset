

```markdown
- Start EMAC_CORE reception by setting `EMACRX` to 1.
- Detect the `RECV_INT` interrupt if enabled, and wait for the frame reception to complete.

## 52.5.5 TX Entering and Exiting the LPI State

- Configure the LPI timer counter via `EMACLPTIMERSCONTROL_REG`
- Make the transmitter to enter the LPI state via `EMACLPI_CSR_REG`
- Detect the `LPI_INT` interrupt, and wait for `TLPIEN` to be set, which indicates that the transmitter has entered the LPI state
- Bring the transmitter out of the LPI state by clearing `LPIEN`
- Detect the `LPI_INT` interrupt, and wait for `TLPIEX` to be set, which indicates that the transmitter has exited the LPI state

## 52.5.6 RX Entering and Exiting the LPI State

- Detect the `LPI_INT` interrupt, and wait for `RLPIEN` to be set, which indicates that the receiver has entered the LPI state
- Detect the `LPI_INT` interrupt, and wait for `RLPIEX` to be set, which indicates that the receiver has exited the LPI state

## 52.6 Interrupts

ESP32-P4's EMAC can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

- `ETH_MAC_INTR`
- `PMT_INTR`
- `LPT_INTR`

There are several internal interrupt sources from EMAC that can generate the above interrupt signals.

The following interrupt sources can generate the `ETH_MAC_INTR` interrupt signal:

- `ABN_INT_SUMM`: Triggered when `DMAINT_AISE` is 1 and the following interrupts are triggered.
    - `TRANS_PROC_STOP`: Triggered when `DMAINT_TSE` is 1 and the transmit process stops.
    - `TRANS_JABBER_TO`: Triggered when `DMAINT_TJTE` is 1 and the frame size exceeds 2048 bytes (10240 bytes if the jumbo frame is enabled).
    - `RECV_OVFLOW`: Triggered when `DMAINT_OIE` is 1 and the receive buffer overflows during frame reception.
    - `TRANS_UNDFLOW`: Triggered when `DMAINT_UIE` is 1 and the transmit buffer underflows during frame transmission.
    - `RECV_BUF_UNAVAIL`: Triggered when `DMAINT_RBUE` is 1, the Host owns the Next Descriptor in the Receive List and the DMA cannot acquire it.
    - `RECV_PROC_STOP`: Triggered when `DMAINT_RSE` is 1 and the receive process stops.
```