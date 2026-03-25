

```markdown
Chapter 28 I2S Controller (I2S)
GoBack

## 28.13.2 Configure I2S as RX Mode

Follow the steps below to configure I2S as RX mode via software:

1. Configure the clock as described in Section 28.6.
2. Configure signal pins according to Table 28.4-1.
3. Select the mode needed by configuring `I2S_RX_SLAVE_MOD`.
    *   0: Master RX mode
    *   1: Slave RX mode
4. Set needed RX data mode and RX channel mode as described in Section 28.10, and then set `I2S_RX_UPDATE`.
5. Reset the RX unit and its FIFO according to Section 28.7.
6. Enable the corresponding interrupts. See Section 28.12.
7. Configure GDMA inlink and set the length of RX data by configuring `I2S_RX_EOF_NUM_REG`.
8. Start receiving data:
    *   In master mode, when the slave is ready, set `I2S_RX_START` to start receiving data.
    *   In slave mode, set `I2S_RX_START` to start receiving data when BCK and WS signals are received from the master.
9. The received data is then stored to the specified memory address according to the configuration of GDMA. Then the corresponding interrupt set in step 6 is generated.
```