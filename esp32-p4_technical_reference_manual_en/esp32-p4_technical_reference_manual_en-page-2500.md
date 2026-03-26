

```markdown
Chapter 47 LP I2S Controller

GoBack

reception is suspended, if LP_I2S_RX_START is not cleared, data reception can be restarted by setting LP_I2S_RX_RESET to 1.
- RX unit stops receiving data when the bit LP_I2S_RX_START is cleared.

• LP I2S works as a slave receiver:
    - Set LP_I2S_RX_START. Wait for the master BCK signal to start receiving data.
    - Configure LP_I2S_RX_STOP_MODE to control data reception suspension:

        * 0: The RX unit only suspends data reception when LP_I2S_RX_START is cleared.
        * 1: The RX unit suspends data reception when LP_I2S_RX_START is cleared or the number of received bytes is greater than the value configured in LP_I2S_RX_EOF_NUM_REG. After data reception is suspended, if LP_I2S_RX_START is not cleared, data reception can be restarted by setting LP_I2S_RX_RESET to 1.

    - The RX unit stops receiving data when the bit LP_I2S_RX_START is cleared.

47.8 Receiving Data

In RX mode, LP I2S first reads data from the peripheral interface and then stores the data in the LP I2S memory according to the configured channel mode and data mode.

47.8.1 Channel Mode Control

ESP32-P4 LP I2S supports both TDM RX mode and PDM RX mode. Set LP_I2S_RX_TDM_EN to enable TDM RX mode, or set LP_I2S_RX_PDM_EN to enable PDM RX mode.

Note:
LP_I2S_RX_TDM_EN and LP_I2S_RX_PDM_EN must not be cleared or set simultaneously.

47.8.1.1 TDM RX Mode

In TDM RX mode, LP I2S supports up to 2 channels to input data. The total number of RX channels in use is controlled by LP_I2S_RX_TDM_TOT_CHAN_NUM. For example, if LP_I2S_RX_TDM_TOT_CHAN_NUM is set to 1, channel 0 ~ 1 will be used to receive data.

In these RX channels, if LP_I2S_RX_TDM_PDM_CHANn_EN is set to:

    • 0: The channel data is invalid and will not be stored into RX FIFO;
    • 1: The channel data is valid and will be stored into RX FIFO.

In TDM master mode, WS signal is controlled by LP_I2S_RX_WS_IDLE_POL and LP_I2S_RX_TDM_WS_WIDTH.

    • LP_I2S_RX_WS_IDLE_POL: The default level of WS signal;
    • LP_I2S_RX_TDM_WS_WIDTH: The cycles the WS default level lasts for when receiving all channel data.
LP_I2S_RX_HALF_SAMPLE_BITS x 2 is equal to the BCK cycles in one WS period.

Espressif Systems
2500
ESP32-P4 TRM
PRELIMINARY

Submit Documentation Feedback
```