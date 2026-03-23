

```markdown
Configure I2S_RX_PCM_CONF:

*   0: decompress the data using A-law
*   1: compress the data using A-law
*   2: decompress the data using μ-law
*   3: compress the data using μ-law

At this point, the data format control is completed. Data then is stored into memory via DMA.

## 30.11 Software Configuration Process

### 30.11.1 Configure I2S as TX Mode

Follow the steps below to configure I2S as TX mode via software:

1.  Configure the clock as described in Section 30.6.
2.  Configure signal pins according to Table 30.4-1.
3.  Select the mode needed by configuring I2S_TX_SLAVE_MOD.

    *   0: master TX mode
    *   1: slave TX mode

4.  Set needed TX data mode and TX channel mode as described in Section 30.9, and then set I2S_TX_UPDATE.
5.  Reset TX unit and TX FIFO as described in Section 30.7.
6.  Enable corresponding interrupts. See Section 30.12.
7.  Configure DMA outlink.
8.  Set I2S_TX_STOP_EN if needed. For more information, please refer to Section 30.8.1.
9.  Start transmitting data:

    *   In master mode, wait till I2S slave gets ready, then set I2S_TX_START to start transmitting data.
    *   In slave mode, set I2S_TX_START. When the I2S master supplies BCK and WS signals, I2S slave starts transmitting data.

10. Wait for the interrupt signals set in Step 6, or check whether the transfer is completed by querying I2S_TX_IDLE:

    *   0: transmitter is working;
    *   1: transmitter is in idle state.

11. Clear I2S_TX_START to stop data transfer.

### 30.11.2 Configure I2S as RX Mode

Follow the steps below to configure I2S as RX mode via software:

1.  Configure the clock as described in Section 30.6.
```