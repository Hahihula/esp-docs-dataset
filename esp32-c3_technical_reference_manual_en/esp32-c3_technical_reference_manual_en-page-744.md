

```markdown
| Channel Control Option | Left Channel | Right Channel | Mode Control Field¹ | Channel Select Bit² |
|------------------------|--------------|---------------|---------------------|--------------------|
| Stereo mode            | Transmit the left channel data | Transmit the right channel data | 0 | x |
|                        | Transmit the left channel data | Transmit the left channel data | 1 | 0 |
|                        | Transmit the right channel data | Transmit the right channel data | 1 | 1 |
|                        | Transmit the right channel data | Transmit the right channel data | 2 | 0 |
| Mono mode              | Transmit the left channel data | Transmit the left channel data | 2 | 1 |
|                        | Transmit the value of “single”³ | Transmit the right channel data | 3 | 0 |
|                        | Transmit the left channel data | Transmit the value of “single” | 3 | 1 |
|                        | Transmit the left channel data | Transmit the value of “single” | 4 | 0 |
|                        | Transmit the value of “single” | Transmit the right channel data | 4 | 1 |

¹ I2S_TX_CHAN_MOD
² I2S_TX_WS_IDLE_POL
³ The “single” value is equal to the value of I2S_SINGLE_DATA.
```

Table 29.9-5. PCM-to-PDM TX Mode

| Channel Output Format | I2S_TX_PDM_DAC_MODE_EN | I2S_TX_PDM_DAC_2OUT_EN |
|-----------------------|------------------------|-------------------------|
| 1-line PDM output format¹ | 0 | x |
| 1-line DAC output format² | 1 | 0 |
| 2-line DAC output format | 1 | 1 |

Note:
1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.

• Configure sampling frequency and upsampling rate

In PCM-to-PDM TX mode, PDM clock frequency is equal to BCK frequency. The relation of sampling frequency (fSampling) and BCK frequency is as follows:

```latex
f_{\text{Sampling}} = \frac{f_{\text{BCK}}}{\text{OSR}}
```
```