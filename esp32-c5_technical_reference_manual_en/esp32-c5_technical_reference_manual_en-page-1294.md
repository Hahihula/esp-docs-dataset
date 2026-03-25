

```markdown
| Channel Control Option | Left Channel                                                                 | Right Channel                                                                 | Mode Control Field¹ | Channel Select Bit² |
|------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|---------------------|---------------------|
| Stereo mode            | Transmit the left channel data                                              | Transmit the right channel data                                               | 0                   | x                   |
|                        | Transmit the left channel data                                              | Transmit the left channel data                                                | 1                   | 0                   |
|                        | Transmit the right channel data                                             | Transmit the right channel data                                               | 1                   | 1                   |
| Mono mode              | Transmit the right channel data                                             | Transmit the left channel data                                                | 2                   | 1                   |
|                        | Transmit the value of “single”³                                           | Transmit the right channel data                                               | 3                   | 0                   |
|                        | Transmit the left channel data                                              | Transmit the value of “single”³                                              | 3                   | 1                   |
|                        | Transmit the left channel data                                              | Transmit the value of “single”³                                              | 4                   | 0                   |
|                        | Transmit the value of “single”                                             | Transmit the right channel data                                               | 4                   | 1                   |

¹ I2S_TX_CHAN_MOD
² I2S_TX_WS_IDLE_POL
³ The “single” value is equal to the value of I2S_SINGLE_DATA.
```

If the PCM-to-PDM converter is enabled, the PCM data through GDMA is converted to PDM data and then output in PDM signal format. Configure `I2S_PCM2PDM_CONV_EN` to enable the converter. The register configuration for the PCM-to-PDM converter is as follows:

*   Configure 1-line PDM output format or 1-/2-line DAC output mode as the table below:

```markdown
Table 35.9-5. I2S PCM-to-PDM Data Output

| Channel Output Format         | I2S_TX_PDM_DAC_MODE_EN | I2S_TX_PDM_DAC_2OUT_EN |
|-------------------------------|-------------------------|------------------------|
| 1-line PDM output format¹     | 0                       | x                      |
| 1-line DAC output format²     | 1                       | 0                      |
| 2-line DAC output format      | 1                       | 1                      |

Note:
1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.
3. 1-line PDM/DAC output format uses I2SO_Data_out as the data output line.
4. 2-line DAC output format uses I2SO_Data_out and I2SO_Data1_out as data output lines.
5. In terms of application, the PDM output format is targeted at applications that require clock signals and can decode PDM format codecs, while the DAC output format is targeted at applications that do not rely on clock signals, do not have PDM format codecs, and can recover analog waveforms directly through low-pass filtering.
```

*   Configure sampling frequency and upsampling rate as below:
    When the I2S PCM-to-PDM converter is enabled, PDM clock frequency is equal to BCK frequency. The relation of sampling frequency (fSampling, the sampling frequency of PCM data) and BCK frequency (the
```