

```markdown
I2S_TX_FIFO_CNT value of each device to determine the location of the audio data being sent to perform synchronization.

2. I2S TX stability check
When the device is in an application scenario with high GDMA usage, there may be numbers missing in I2S TX occasionally due to multiplexing arbitration. In this case, check the ratio of `I2S_TX_BCK_CNT` to `I2S_TX_FIFO_CNT` to confirm the stability of the device when running I2S TX.

## 46.10 Receiving Data

In RX mode, I2Sn first reads data from the peripheral interface and then stores the data in memory via GDMA according to the configured channel mode and data mode.

### 46.10.1 Channel Mode Control

ESP32-P4 I2Sn supports both TDM RX mode and PDM RX mode. Set `I2S_RX_TDM_EN` to enable TDM RX mode, or set `I2S_RX_PDM_EN` to enable PDM RX mode.

**Note:**
```
I2S_RX_TDM_EN and I2S_RX_PDM_EN must not be cleared or set simultaneously.
```

#### 46.10.1.1 TDM RX Mode

In TDM RX mode, I2Sn supports up to 16 channels to input data. The total number of RX channels in use is controlled by `I2S_RX_TDM_TOT_CHAN_NUM`. For example, if `I2S_RX_TDM_TOT_CHAN_NUM` is set to 5, channel O ~ 5 will be used to receive data.

In these RX channels, if `I2S_RX_TDM_CHANn_EN` is set to:

*   1: The channel data is valid and will be stored into RX FIFO;
*   0: The channel data is invalid and will not be stored into RX FIFO.

In TDM master mode, WS signal is controlled by `I2S_RX_WS_IDLE_POL` and `I2S_RX_TDM_WS_WIDTH`.

```
I2S_RX_WS_IDLE_POL: The default level of WS signal;
I2S_RX_TDM_WS_WIDTH: The cycles the WS default level lasts for when receiving all channel data.
```

`I2S_RX_HALF_SAMPLE_BITS x 2` is equal to the BCK cycles in one WS period.

#### 46.10.1.2 PDM RX Mode

In PDM RX mode, I2Sn supports both PDM raw data reception and PDM-to-PCM data format conversion (the latter only supported by I2SO).

In PDM RX mode, I2Sn converts the serial data from channels to the data to be entered into memory.

In PDM RX master mode, the default level of the WS signal is controlled by `I2S_RX_WS_IDLE_POL`. WS frequency is half of the BCK frequency. The configuration of the BCK signal is similar to that of WS signal as described in Section 46.6. Note, in PDM RX mode, the value of `I2S_RX_HALF_SAMPLE_BITS` must be same as that of `I2S_RX_BITS_MOD`.
```