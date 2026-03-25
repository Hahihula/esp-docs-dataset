

```markdown
## 28.11 Event Task Matrix Feature

ESP32-C61 I2S supports the Event Task Matrix (ETM) function, which allows I2S’s ETM tasks to be triggered by any peripherals’ ETM events, or I2S’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to I2S. For more information, please refer to Chapter 10 Event Task Matrix (ETM).

I2S can receive the following ETM tasks:

*   `I2SO_TASK_START_TX`: Enables I2S TX for data transfer.
*   `I2SO_TASK_START_RX`: Enables I2S RX for data transfer.
*   `I2SO_TASK_STOP_TX`: Stops I2S TX data transfer.
*   `I2SO_TASK_STOP_RX`: Stops I2S RX data transfer.

I2S can generate the following ETM events:

*   `I2SO_EVT_TX_DONE`: Indicates that I2S TX has completed data transmission. Triggered when all data in the TX FIFO has been sent.
*   `I2SO_EVT_RX_DONE`: Can be triggered in different ways depending on the configured value of `I2S_RX_STOP_MODE`:
    *   0: Will not be triggered;
    *   1: When triggered, indicates that the number of bytes received by I2S RX is greater than the receive length value configured by `I2S_RX_EOF_NUM_REG`;
    *   2: When triggered, indicates that the GDMA RX FIFO is full.
*   `I2SO_EVT_X_WORDS_SENT`: Indicates that the word number sent by I2S TX is equal to or larger than the value set by `I2S_ETM_TX_SEND_WORD_NUM`.
*   `I2SO_EVT_X_WORDS_RECEIVED`: Indicates that the word number received by I2S RX is equal to or larger than the value set by `I2S_ETM_RX_RECEIVE_WORD_NUM`.

In practical applications, I2S’s ETM events can trigger its own ETM tasks. For example, the `I2SO_EVT_X_WORDS_SENT` event can trigger the `I2SO_TASK_STOP_TX` task, and in this way stop the I2S operation through ETM.

## 28.12 I2S Interrupts

ESP32-C61’s I2S can generate the `I2S_INTR` interrupt signal that will be sent to the Interrupt Matrix. There are several internal interrupt sources from I2S that can generate the above interrupt signal(s) as follows:

*   `I2S_TX_HUNG_INT`: Triggered when data transmission is timed out. For example, if the I2S module is configured as TX slave mode, but the master does not provide BCK or WS signals for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
*   `I2S_RX_HUNG_INT`: Triggered when the data reception is timed out. For example, if the I2S module is configured as RX slave mode, but the master does not transmit data for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
```