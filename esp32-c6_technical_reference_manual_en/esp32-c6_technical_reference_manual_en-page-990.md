

```markdown
WS(LRCK)

SD(SDOUT)—

Left Left

Data (Left) = Data (Right)

I2S_TX_CHAN_MOD = 2; I2S_TX_WS_IDLE_POL = 1;

Figure 30.9-3. PDM Channel Control Example


## 30.10 Receiving Data

In RX mode, I2S first reads data from peripheral interface, and then stores the data into memory via DMA according to the configured channel mode and data mode.

### 30.10.1 Channel Mode Control

ESP32-C6 I2S supports both TDM RX mode and PDM RX mode. Set `I2S_RX_TDM_EN` to enable TDM RX mode, or set `I2S_RX_PDM_EN` to enable PDM RX mode.

**Note:**
```
I2S_RX_TDM_EN and I2S_RX_PDM_EN must not be cleared or set simultaneously.
```


### 30.10.1.1 I2S Channel Control in TDM RX Mode

In TDM RX mode, the total number of RX channels supported is related to the channel valid data width for I2S as follows:

Table 30.10-1. The Matching Between Valid Data Width and Number of RX Channel Supported

| Channel Valid Data Width | Total Number of Channels Supported |
|--------------------------|-------------------------------------|
| 32                       | 4                                   |
| 24                       | 5                                   |
| 16                       | 8                                   |
| 8                        | 16                                  |

In TDM RX mode, I2S supports up to 16 channels to input data. The total number of RX channels in use is controlled by `I2S_RX_TDM_TOT_CHAN_NUM`. For example, if `I2S_RX_TDM_TOT_CHAN_NUM` is set to 5,
```