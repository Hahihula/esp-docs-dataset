

```markdown
I2S_TX_BITS_MOD = 23

I2S_TX_BIG_ENDIAN = 1

I2S_TX_TDM_CHAN_BITS = 31  
I2S_TX_LEFT_ALIGN = 1

I2S_TX_BIT_ORDER = 1

Figure 35.9-1. TX Data Format Control
```

## 35.9.2 Channel Mode Control

ESP32-C5 I2S supports both TDM TX mode and PDM TX mode. Set `I2S_TX_TDM_EN` to enable TDM TX mode, or set `I2S_TX_PDM_EN` to enable PDM TX mode.

**Note:**
```
I2S_TX_TDM_EN and I2S_TX_PDM_EN must not be cleared or set simultaneously.
```

### 35.9.2.1 TDM TX Mode

In TDM TX mode, I2S supports up to 16 channels to transmit data. The total number of TX channels in use is controlled by `I2S_TX_TDM_TOT_CHAN_NUM`. For example, if `I2S_TX_TDM_TOT_CHAN_NUM` is set to 5, six channels in total (channel O-5) will be used to transmit data. See Figure 35.9-2.

**Note:**
```
Most stereo I2S codecs can be controlled by setting the I2S module into 2-channel mode under TDM standard.
```

In these TX channels, if `I2S_TX_TDM_CHANn_EN` is set to:

*   1: This channel transmits the channel data out;
*   0: The TX data to be sent by this channel is controlled by `I2S_TX_CHAN_EQUAL`:
    *   -1: The data of the previous channel is sent out;
    *   -0: The data stored in `I2S_SINGLE_DATA` is sent out.

In TDM TX master mode, WS signal is controlled by `I2S_TX_WS_IDLE_POL` and `I2S_TX_TDM_WS_WIDTH`:

*   `I2S_TX_WS_IDLE_POL`: The default level of WS signal;
*   `I2S_TX_TDM_WS_WIDTH`: The cycles the WS default level lasts for when transmitting all channel data.
```