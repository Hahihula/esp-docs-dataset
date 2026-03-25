

```markdown
- I2S_TX_DONE_INT: Triggered when sending data is complete, i.e., all data in I2S TX FIFO has been sent.
- I2S_RX_DONE_INT: Triggered when the data receiving is completed.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 9 Interrupt Matrix > Section 9.2 Interrupt Terminology in ESP32-C61.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 28.14 Register Summary.
```

## 28.13 Software Configuration Process

### 28.13.1 Configure I2S as TX Mode

Follow the steps below to configure I2S as TX mode via software:

1. Configure the clock as described in Section 28.6.

2. Configure signal pins according to Table 28.4-1.

3. Select the mode needed by configuring `I2S_TX_SLAVE_MOD`.
   - 0: Master TX mode
   - 1: Slave TX mode

4. Set needed TX data mode and TX channel mode as described in Section 28.9, and then set `I2S_TX_UPDATE`.

5. Reset TX unit and TX FIFO as described in Section 28.7.

6. Enable corresponding interrupts. See Section 28.12.

7. Configure DMA outlink.

8. Set `I2S_TX_STOP_EN` if needed. For more information, please refer to Section 28.8.1.

9. Start transmitting data:
   - In master mode, wait till I2S slave gets ready, then set `I2S_TX_START` to start transmitting data;
   - In slave mode, set `I2S_TX_START`. When the I2S master supplies BCK and WS signals, I2S slave starts transmitting data.

10. Wait for the interrupt signals set in Step 6, or check whether the transfer is completed by querying `I2S_TX_IDLE`:
    - 0: Transmitter is working;
    - 1: Transmitter is in idle state.

11. Clear `I2S_TX_START` to stop data transfer.
```