

```markdown
Note:
1. The data above refers to the processed data after data format control instead of the original data.
2. "Left" and "Right" represent channel data, and their bit widths are channel valid data width. Please refer to Section 28.9.1.

Then the channel data is transmitted after channel mode control as follows.

WS(LRCK)
SD(SDOUT)

Data (Left) = Data (Right)

I2S_TX_CHAN_MOD = 2; I2S_TX_WS_IDLE_POL = 1;

Figure 28.9-3. PDM Channel Control Example

28.10 Receiving Data

In RX mode, I2S first reads data from the peripheral interface and then stores the data in memory via GDMA according to the configured channel mode and data mode.

28.10.1 Channel Mode Control

ESP32-C61 I2S supports both TDM RX mode and PDM RX mode. Set I2S_RX_TDM_EN to enable TDM RX mode, or set I2S_RX_PDM_EN to enable PDM RX mode.

Note:
I2S_RX_TDM_EN and I2S_RX_PDM_EN must not be cleared or set simultaneously.

28.10.1.1 TDM RX Mode

In TDM RX mode, I2S supports up to 16 channels to input data. The total number of RX channels in use is controlled by I2S_RX_TDM_TOT_CHAN_NUM. For example, if I2S_RX_TDM_TOT_CHAN_NUM is set to 5, channel 0-5 will be used to receive data.

In these RX channels, if I2S_RX_TDM_CHANn_EN is set to:
• 1: The channel data is valid and will be stored into RX FIFO;
```