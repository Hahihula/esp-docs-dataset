

```markdown
8. Set I2S_TX_STOP_EN if needed. For more information, please refer to Section 35.8.1.
9. Start transmitting data:
    * In master mode, wait till I2S slave gets ready, then set I2S_TX_START to start transmitting data;
    * In slave mode, set I2S_TX_START. When the I2S master supplies BCK and WS signals, I2S slave starts transmitting data.
10. Wait for the interrupt signals set in Step 6, or check whether the transfer is completed by querying I2S_TX_IDLE:
    * 0: Transmitter is working;
    * 1: Transmitter is in idle state.
11. Clear I2S_TX_START to stop data transfer.

35.13.2 Configure I2S as RX Mode

Follow the steps below to configure I2S as RX mode via software:

1. Configure the clock as described in Section 35.6.
2. Configure signal pins according to Table 35.4-1.
3. Select the mode needed by configuring I2S_RX_SLAVE_MOD.
    * 0: Master RX mode
    * 1: Slave RX mode
4. Set needed RX data mode and RX channel mode as described in Section 35.10, and then set I2S_RX_UPDATE.
5. Reset the RX unit and its FIFO according to Section 35.7.
6. Enable the corresponding interrupts. See Section 35.12.
7. Configure GDMA inlink and set the length of RX data by configuring I2S_RX_EOF_NUM_REG.
8. Start receiving data:
    * In master mode, when the slave is ready, set I2S_RX_START to start receiving data.
    * In slave mode, set I2S_RX_START to start receiving data when BCK and WS signals are received from the master.
9. The received data is then stored to the specified memory address according to the configuration of GDMA. Then the corresponding interrupt set in step 6 is generated.
```