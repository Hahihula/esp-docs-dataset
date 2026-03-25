

```markdown
## 28.9.2.2 PDM TX Mode

In PDM TX mode, I2S supports both PDM raw data transmission and PCM-to-PDM data format conversion.

In PDM TX mode, fetching data through GDMA is controlled by `I2S_TX_MONO` and `I2S_TX_MONO_FST_VLD`. See Table 28.9-3. Configure the two bits according to the data stored in memory, be it the single-channel or dual-channel data.

Table 28.9-3. Data-Fetching Control in PDM Mode

| Data-Fetching Control Option | Mode       | I2S_TX_MONO | I2S_TX_MONO_FST_VLD |
|------------------------------|------------|-------------|---------------------|
| Post data-fetching request to GDMA at any edge of WS signal               | Stereo mode | 0           | x                   |
| Post data-fetching request to GDMA only at the second half period of WS signal | Mono mode   | 1           | 0                   |
| Post data-fetching request to GDMA only at the first half period of WS signal | Mono mode   | 1           | 1                   |

When I2S is in PDM TX master mode, the default level of WS signal is controlled by `I2S_TX_WS_IDLE_POL`, and the WS signal frequency is half of the BCK signal frequency. The configuration of WS signal is similar to that of BCK signal. Please refer to Section 28.6 and Figure 28.6.

When transmitting raw PDM data, the I2S channel mode is controlled by `I2S_TX_CHAN_MOD` and `I2S_TX_WS_IDLE_POL`. See the table below.

Table 28.9-4. I2S Channel Control for Raw PDM Data

| Channel Con- trol Option | Left Channel                                                                 | Right Channel                          | Mode Control Field¹ | Channel Select Bit² |
|--------------------------|------------------------------------------------------------------------------|----------------------------------------|---------------------|---------------------|
| Stereo mode              | Transmit the left channel data                                              | Transmit the right channel data       | 0                   | x                   |
|                          | Transmit the left channel data                                              | Transmit the left channel data        | 1                   | 0                   |
|                          | Transmit the right channel data                                             | Transmit the right channel data       | 1                   | 1                   |
|                          | Transmit the right channel data                                             | Transmit the right channel data       | 2                   | 0                   |
| Mono mode                | Transmit the left channel data                                              | Transmit the left channel data        | 2                   | 1                   |
|                          | Transmit the value of "single"³                                           | Transmit the right channel data       | 3                   | 0                   |
|                          | Transmit the left channel data                                              | Transmit the value of "single"³      | 3                   | 1                   |
|                          | Transmit the left channel data                                              | Transmit the value of "single"³      | 4                   | 0                   |
|                          | Transmit the value of "single"³                                           | Transmit the right channel data       | 4                   | 1                   |

¹ `I2S_TX_CHAN_MOD`
² `I2S_TX_WS_IDLE_POL`
³ The "single" value is equal to the value of `I2S_SINGLE_DATA`.

If the PCM-to-PDM converter is enabled, the PCM data through GDMA is converted to PDM data and then output in PDM signal format. Configure `I2S_PCM2PDM_CONV_EN` to enable the converter. The register configuration for the PCM-to-PDM converter is as follows:

*   Configure 1-line PDM output format or 1-/2-line DAC output mode as the table below:
```