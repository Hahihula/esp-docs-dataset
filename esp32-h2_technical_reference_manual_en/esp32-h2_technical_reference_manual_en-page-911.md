

```markdown
| Channel Output Format | I2S_TX_PDM_DAC_MODE_EN | I2S_TX_PDM_DAC_2OUT_EN |
|-----------------------|-------------------------|--------------------------|
| 1-line PDM output format¹ | 0                       | X                        |
| 1-line DAC output format² | 1                       | 0                        |
| 2-line DAC output format   | 1                       | 1                        |

Note:
1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.
3. 1-line PDM/DAC output format uses I2SO_Data_out as the data output line.
4. 2-line DAC output format uses I2SO_Data_out and I2SO_Data1_out as data output lines.
5. In terms of application, the PDM output format is targeted at applications that require clock signals and can decode PDM format codecs, while the DAC output format is targeted at applications that do not rely on clock signals, do not have PDM format codecs, and can recover analog waveforms directly through low-pass filtering.

• Configure sampling frequency and upsampling rate as below:
When the I2S PCM-to-PDM converter is enabled, PDM clock frequency is equal to BCK frequency. The relation of sampling frequency ($f_{Sampling}$, the sampling frequency of PCM data) and BCK frequency (the sampling frequency of PDM data) is as follows:

$$
f_{Sampling} = \frac{f_{BCK}}{\text{OSR}}
$$

Upsampling rate (OSR) is related to I2S_TX_PDM_SINC_OSR2 as follows:

$$
\text{OSR} = \text{I2S_TX_PDM_SINC_OSR2} \times 64
$$

Sampling frequency $f_{Sampling}$ is related to I2S_TX_PDM_FS as follows:

$$
f_{Sampling} = \text{I2S_TX_PDM_FS} \times 100
$$

Configure the registers according to the needed sampling frequency, upsampling rate, and PDM clock frequency.

PDM Channel Configuration Example

In this example, the register configuration is as follows.
• I2S_PCM2PDM_CONV_EN = 0, i.e., transmit the raw PDM data.
• I2S_TX_MONO = 0, i.e., data is fetched from memory via GDMA in both the high and low levels of WS.
• I2S_TX_CHAN_MOD = 2, i.e., mono mode is selected.
• I2S_TX_WS_IDLE_POL = 1, i.e., both the left and right channels transmit the left channel data, and the right channel data will be discarded.

Once the configuration is done, assume that the data in memory after data format control is:

Left | Right | Left | Right | ... | Left | Right
```