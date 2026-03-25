

```markdown
sampling frequency of PDM data) is as follows:

$$f_{\text{sampling}} = \frac{f_{\text{BCK}}}{\text{OSR}}$$

Upsampling rate (OSR) is related to I2S_TX_PDM_SINC_OSR2 as follows:

$$\text{OSR} = \text{I2S_TX_PDM_SINC_OSR2} \times 64$$

Sampling frequency $f_{\text{sampling}}$ is related to I2S_TX_PDM_FS as follows:

$$f_{\text{sampling}} = \text{I2S_TX_PDM_FS} \times 100$$

Configure the registers according to the needed sampling frequency, upsampling rate, and PDM clock frequency.

## PDM Channel Configuration Example

In this example of I2S, the register configuration is as follows.

*   `I2S_PCM2PDM_CONV_EN = 0`, i.e., transmit the raw PDM data.
*   `I2S_TX_MONO = 0`, i.e., data is fetched from memory via GDMA in both the high and low levels of WS.
*   `I2S_TX_CHAN_MOD = 2`, i.e., mono mode is selected.
*   `I2S_TX_WS_IDLE_POL = 1`, i.e., both the left and right channels transmit the left channel data, and the right channel data will be discarded.

Once the configuration is done, assume that the data in memory after data format control is:

| Left | Right | Left | Right | ... | Left | Right |

**Note:**
1.  The data above refers to the processed data after data format control instead of the original data.
2.  “Left” and “Right” represent channel data, and their bit widths are channel valid data width. Please refer to Section 35.9.10

Then the channel data is transmitted after channel mode control as follows.

![Figure 35.9-3. PDM Channel Control Example](image)

I2S_TX_CHAN_MOD = 2; I2S_TX_WS_IDLE_POL = 1;

**Figure 35.9-3. PDM Channel Control Example**
```