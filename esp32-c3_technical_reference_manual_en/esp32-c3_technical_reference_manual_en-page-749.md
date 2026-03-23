

```markdown
Chapter 29 I2S Controller (I2S)

GoBack

• 1: transmitter is in idle.

11. Clear I2S_TX_START to stop data transfer.

## 29.11.2 Configure I2S as RX Mode

Follow the steps below to configure I2S as RX mode via software:

1. Configure the clock as described in Section 29.6.
2. Configure signal pins according to Table 29.4-1.
3. Select the mode needed by configuring the bit I2S_RX_SLAVE_MOD.

    • 0: master RX mode
    • 1: slave RX mode

4. Set needed RX data mode and RX channel mode as described in Section 29.10, and then set the bit I2S_RX_UPDATE.
5. Reset RX unit and its FIFO according to Section 29.7.
6. Enable corresponding interrupts, see Section 29.12.
7. Configure DMA inlink, and set the length of RX data in I2S_RXEOF_NUM_REG.
8. Start receiving data:

    • In master mode, when the slave is ready, set I2S_RX_START to start receiving data.
    • In slave mode, set I2S_RX_START to start receiving data when get BCK and WS signals from the master.

9. The received data is then stored to the specified address of ESP32-C3 memory according the configuration of DMA. Then the corresponding interrupt set in Step 6 is generated.

## 29.12 I2S Interrupts

• I2S_TX_HUNG_INT: triggered when transmitting data is timed out. For example, if module is configured as TX slave mode, but the master does not provide BCK or WS signal for a long time (specified in I2S_LC_HUNG_CO NF_REG), then this interrupt will be triggered.

• I2S_RX_HUNG_INT: triggered when receiving data is timed out. For example, if I2S module is configured as RX slave mode, but the master does not send data for a long time (specified in I2S_LC_HUNG_CONF_REG), then this interrupt will be triggered.

• I2S_TX_DONE_INT: triggered when transmitting data is completed.
• I2S_RX_DONE_INT: triggered when receiving data is completed.

## 29.13 Register Summary

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```