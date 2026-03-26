

```markdown
| Channel Con- | Left Channel | Right Channel | Mode Control Field¹ | Channel Select Bit² |
|--------------|--------------|---------------|---------------------|---------------------|
| trol Option  |              |               |                     |                     |
| Stereo mode  | Transmit the left channel data | Transmit the right channel data | 0 | x |
|              | Transmit the left channel data | Transmit the left channel data | 1 | 0 |
|              | Transmit the right channel data | Transmit the right channel data | 1 | 1 |
|              | Transmit the right channel data | Transmit the right channel data | 2 | 0 |
| Mono mode    | Transmit the left channel data | Transmit the left channel data | 2 | 1 |
|              | Transmit the value of “single”³ | Transmit the right channel data | 3 | 0 |
|              | Transmit the left channel data | Transmit the value of “single” | 3 | 1 |
|              | Transmit the left channel data | Transmit the value of “single” | 4 | 0 |
|              | Transmit the value of “single” | Transmit the right channel data | 4 | 1 |

¹ I2S_TX_CHAN_MOD
² I2S_TX_WS_IDLE_POL
³ The “single” value is equal to the value of I2S_SINGLE_DATA.
```

```markdown
Table 46.9-5. I2SO PCM-to-PDM Data Output

| Channel Output Format | I2S_TX_PDM_DAC_MODE_EN | I2S_TX_PDM_DAC_2OUT_EN |
|-----------------------|------------------------|-------------------------|
| 1-line PDM output format¹ | 0                      | x                       |
| 1-line DAC output format² | 1                      | 0                       |
| 2-line DAC output format | 1                      | 1                       |

Note:
1. In PDM output format, SD data of two channels is sent out in one WS period.
2. In DAC output format, SD data of one channel is sent out in one WS period.
3. 1-line PDM/DAC output format uses I2SnO_Data_out as the data output line.
4. 2-line DAC output format uses I2SnO_Data_out and I2SnO_Data1_out as data output lines.
5. In terms of application, the PDM output format is targeted at applications that require clock signals and can decode PDM format codecs, while the DAC output format is targeted at applications that do not rely on clock signals, do not have PDM format codecs, and can recover analog waveforms directly through low-pass filtering.
```

- Configure sampling frequency and upsampling rate as below:
```markdown
Chapter 46 I2S Controller (I2S) GoBack

When transmitting raw PDM data, the I2Sn channel mode is controlled by I2S_TX_CHAN_MOD and I2S_TX_WS_IDLE_POL. See the table below.

Table 46.9-4. I2Sn Channel Control for Raw PDM Data
```