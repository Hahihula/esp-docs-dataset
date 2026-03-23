

```markdown
Note:

1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.

- Configure sampling frequency and upsampling rate:
  In PCM-to-PDM TX mode, PDM clock frequency is equal to BCK frequency. The relation of sampling
  frequency ($f_{\text{Sampling}}$) and BCK frequency is as follows:

  $$ f_{\text{Sampling}} = \frac{f_{\text{BCK}}}{\text{OSR}} $$

  Upsampling rate (OSR) is related to `I2S_TX_PDM_SINC_OSR2` as follows:

  $$ \text{OSR} = \text{I2S_TX_PDM_SINC_OSR2} \times 64 $$

  Sampling frequency $f_{\text{Sampling}}$ is related to `I2S_TX_PDM_FS` as follows:

  $$ f_{\text{Sampling}} = \text{I2S_TX_PDM_FS} \times 100 $$

Configure the registers according to needed sampling frequency, upsampling rate, and PDM clock
frequency.

PDM Channel Configuration Example

In this example, the register configuration is as follows.

- `I2S_PCM2PDM_CONV_EN` = 0, i.e., the normal PDM TX mode is selected.
- `I2S_TX_MONO` = 0, i.e., data is fetched from memory via DMA in both the high and low levels of WS.
- `I2S_TX_CHAN_MOD` = 2, i.e., mono mode is selected, and the right channel data will be discarded.
- `I2S_TX_WS_IDLE_POL` = 1, i.e., both the left channel and right channel transmit the left channel data.

Once the configuration is done, assume that the data in memory after data format control is:

| Left | Right | Left | Right | ... | Left | Right |

Note:
1. The data above refers to the processed data after data format control instead of the original data.
2. The "Left" and "Right" represent channel data, and their bit widths are channel valid data width. Please refer to
   Section 30.9.10

Then the channel data is transmitted after channel mode control as follows.
```