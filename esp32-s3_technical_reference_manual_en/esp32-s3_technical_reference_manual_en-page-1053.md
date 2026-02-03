**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Body Text:**
The register configuration for PCM-to-PDM output mode is as follows:

- Configure 1-line PDM output format or 1-/2-line DAC output mode as the table below:
  
**Table Title:**
Table 28.9-5. PCM-to-PDM Output Mode

| Channel Output Format | I2S_TX_PDM_DAC_MODE_EN | I2S_TX_PDM_DAC_2OUT_EN |
|-----------------------|-------------------------|--------------------------|
| 1-line PDM output format^1 | O                         | x                          |
| 1-line DAC output format^2 | 0                           | 0                          |
| 2-line DAC output format | 1                           | 1                          |

**Footnotes:**
1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.

- Configure sampling frequency and upsampling rate
  - In PCM-to-PDM mode, PDM clock frequency is equal to BCK frequency. The relation of sampling frequency (f\(_{sampling}\)) and BCK frequency is as follows:
    \[ f_{sampling} = \frac{f_{BCK}}{OSR} \]
  
- Upsampling rate (OSR) is related to I2S_TX_PDM_SINC_OSRS2 as follows:
  - OSR = I2S_TX_PDM_SINC_OSRS2 × 64
  
- Sampling frequency f\(_{sampling}\) is related to I2S_TX_PDM_FS as follows:
  \[ f_{sampling} = \frac{I2S_TX_PDM_FS}{100} \]

Configure the registers according to needed sampling frequency, upsampling rate, and PDM clock frequency.

**Subsection Title:**
PDM Channel Configuration Example

In this example, the register configuration is as follows.
- I2S_TX_CHAN_MOD = 2, i.e., mono mode is selected.
- I2S_TX_WS_IDLE_POL = 1, i.e., both the left channel and right channel transmit the left channel data.

Once the configuration is done, the channel data is transmitted as follows:

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)