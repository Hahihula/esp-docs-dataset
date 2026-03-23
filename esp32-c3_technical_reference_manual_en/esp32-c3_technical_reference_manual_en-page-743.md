

```markdown
I2S_TX_TDM_CHANNEL_NUM = 5; I2S_TX_CHANNEL_EQUAL = 1;
I2S_TX_TDM_CHANNEL1_EN = 0; I2S_TX_TDM_CHANNEL2_EN = 1;
I2S_TX_TDM_CHANNEL3_EN = 0; I2S_TX_TDM_CHANNEL4_EN = 0;
I2S_TX_TDM_CHANNEL5_EN = 1;

Figure 29.9-2. TDM Channel Control

## 29.9.2.2 I2S Channel Control in PDM TX Mode

ESP32-C3 I2S supports two PDM TX modes, namely, normal PDM TX mode and PCM-to-PDM TX mode. In PDM TX mode, fetching data from DMA is controlled by `I2S_TX_MONO` and `I2S_TX_MONO_FST_VLD`, see Table 29.9-3. Please configure the two bits according to the data stored in memory, be it the single-channel or dual-channel data.

Table 29.9-3. Data-Fetching Control in PDM TX Mode

| Data-Fetching Control Option | Mode       | I2S_TX_MONO | I2S_TX_MONO_FST_VLD |
|-------------------------------|------------|-------------|----------------------|
| Post data-fetching request to DMA at any edge of WS signal | Stereo mode | 0           | x                    |
| Post data-fetching request to DMA only at the second half period of WS signal | Mono mode   | 1           | 0                    |
| Post data-fetching request to DMA only at the first half period of WS signal | Mono mode   | 1           | 1                    |

In normal PDM TX mode, I2S channel mode is controlled by `I2S_TX_CHANNEL_MOD` and `I2S_TX_WS_IDLE_POL`, see the table below.
```