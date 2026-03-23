

```markdown
I2S_TX_BITS_MOD = 23

I2S_TX_BIG_ENDIAN = 1

I2S_TX_TDM_CHAN_BITS = 31
I2S_TX_LEFT_ALIGN = 1

I2S_TX_BIT_ORDER = 1

Figure 30.9-1. TX Data Format Control

30.9.2 Channel Mode Control

ESP32-C6 I2S supports both TDM TX mode and PDM TX mode. Set `I2S_TX_TDM_EN` to enable TDM TX mode, or set `I2S_TX_PDM_EN` to enable PDM TX mode.

Note:
*   `I2S_TX_TDM_EN` and `I2S_TX_PDM_EN` must not be cleared or set simultaneously.
*   Most stereo I2S codecs can be controlled by setting the I2S module into 2-channel mode under TDM standard.

30.9.2.1 I2S Channel Control in TDM TX Mode

In TDM TX mode, the total number of TX channels supported is related to the channel valid data width for I2S as follows:

Table 30.9-3. The Matching Between Valid Data Width and Number of TX Channel Supported

| Channel Valid Data Width | Total Number of Channels Supported |
|--------------------------|-------------------------------------|
| 32                       | 4                                   |
| 24                       | 5                                   |
| 16                       | 8                                   |
| 8                        | 16                                  |

The total number of TX channels in use is controlled by `I2S_TX_TDM_TOT_CHAN_NUM`. For example, if `I2S_TX_TDM_TOT_CHAN_NUM` is set to 5, six channels in total (channel 0 ~ 5) will be used to transmit data. See Figure 30.9-2.
```