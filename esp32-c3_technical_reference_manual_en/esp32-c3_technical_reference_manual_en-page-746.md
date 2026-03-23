

```markdown
Note:
I2S_RX_TDM_EN and I2S_RX_PDM_EN must not be cleared or set simultaneously.

## 29.10.1.1 I2S Channel Control in TDM RX Mode

In TDM RX mode, I2S supports up to 16 channels to input data. The total number of RX channels in use is controlled by `I2S_RX_TDM_TOT_CHAN_NUM`. For example, if `I2S_RX_TDM_TOT_CHAN_NUM` is set to 5, channel 0 ~ 5 will be used to receive data.

In these RX channels, if `I2S_RX_TDM_CHANn_EN` is set to:

*   1: this channel data is valid and will be stored into RX FIFO.
*   0: this channel data is invalid and will not be stored into RX FIFO.

In TDM RX master mode, WS signal is controlled by `I2S_RX_WS_IDLE_POL` and `I2S_RX_TDM_WS_WIDTH`.

*   `I2S_RX_WS_IDLE_POL`: the default level of WS signal
*   `I2S_RX_TDM_WS_WIDTH`: the cycles the WS default level lasts for when receiving all channel data

`I2S_RX_HALF_SAMPLE_BITS x 2` is equal to the BCK cycles in one WS period.

## 29.10.1.2 I2S Channel Control in PDM RX Mode

In PDM RX mode, I2S converts the serial data from channels to the data to be entered into memory.

In PDM RX master mode, the default level of WS signal is controlled by `I2S_RX_WS_IDLE_POL`. WS frequency is half of BCK frequency. The configuration of BCK signal is similar to that of WS signal as described in Section 29.6. Note, in PDM RX mode, the value of `I2S_RX_HALF_SAMPLE_BITS` must be same as that of `I2S_RX_BITS_MOD`.

## 29.10.2 Data Format Control

Data format is controlled in the following phases:

*   Phase I: serial input data is converted into the data to be saved to RX FIFO.
*   Phase II: the data is read from RX FIFO and converted according to input data mode.

### 29.10.2.1 Bit Order Control of Channel Data

The channel data will be stored as the data to be input in order from high to low. The data bit order in each channel is controlled by `I2S_RX_BIT_ORDER`:

*   0: The bit order of the data to be input is not reversed;
*   1: The bit order of the data to be input is reversed.

At this point, the first phase of data format control is complete.
```