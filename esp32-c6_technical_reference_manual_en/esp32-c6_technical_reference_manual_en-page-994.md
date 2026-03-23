

```markdown
2. Configure signal pins according to Table 30.4-1.
3. Select the mode needed by configuring I2S_RX_SLAVE_MOD.
    * 0: master RX mode
    * 1: slave RX mode
4. Set needed RX data mode and RX channel mode as described in Section 30.10, and then set I2S_RX_UPDATE.
5. Reset RX unit and its FIFO according to Section 30.7.
6. Enable corresponding interrupts. See Section 30.12.
7. Configure DMA inlink, and set the length of RX data by configuring I2S_RX_EOF_NUM_REG.
8. Start receiving data:
    * In master mode, when the slave is ready, set I2S_RX_START to start receiving data.
    * In slave mode, set I2S_RX_START to start receiving data when get BCK and WS signals from the master.
9. The received data is then stored to the specified address of ESP32-C6 memory according the configuration of DMA. Then the corresponding interrupt set in step 6 is generated.

## 30.12 I2S Interrupts

* I2S_TX_HUNG_INT: triggered when transmitting data is timed out. For example, if module is configured as TX slave mode, but the master does not provide BCK or WS signal for a long time (specified in I2S_LC_HUNG_CONF_REG), then this interrupt will be triggered.
* I2S_RX_HUNG_INT: triggered when receiving data is timed out. For example, if I2S module is configured as RX slave mode, but the master does not send data for a long time (specified in I2S_LC_HUNG_CONF_REG), then this interrupt will be triggered.
* I2S_TX_DONE_INT: triggered when transmitting data is completed.
* I2S_RX_DONE_INT: triggered when receiving data is completed.

## 30.13 Event Task Matrix Feature

ESP32-C6 I2S supports the Event Task Matrix (ETM) function, which allows I2S's ETM tasks to be triggered by any peripherals' ETM events, or I2S's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to I2S. For more information, please refer to Chapter 11 Event Task Matrix (SOC_ETM).

I2S can receive the following ETM tasks:
* I2S_TASK_START_TX: Enables I2S TX for data transfer.
* I2S_TASK_START_RX: Enables I2S RX for data transfer.
* I2S_TASK_STOP_TX: Stops I2S TX data transfer.
```