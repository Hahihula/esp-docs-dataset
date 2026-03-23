

```markdown
Register 29.8. I2S_TX_PCM2PDM_CONF_REG (0x0040)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                    |
| 30  | I2S_TX_PDM_SINC_OSR2                                                       |
| 29  | I2S_PCM2PDM_CONV_EN                                                        |
| 28  | I2S_TX_PDM_DAC_MODE_EN                                                    |
| 27  | I2S_TX_PDM_DAC_2OUT_EN                                                    |
| 5   | reserved                                                                   |
| 4   | (reserved)                                                                 |
| 3   | 0x2                                                                        |
| 2   | 0                                                                          |
| 1   | Reset                                                                      |

I2S_TX_PDM_SINC_OSR2 I2S TX PDM OSR value. (R/W)

I2S_TX_PDM_DAC_2OUT_EN 0: 1-line DAC output mode. 1: 2-line DAC output mode. Only valid when I2S_TX_PDM_DAC_MODE_EN is set. (R/W)

I2S_TX_PDM_DAC_MODE_EN 0: 1-line PDM output mode. 1: DAC output mode. (R/W)

I2S_PCM2PDM_CONV_EN Enable bit for I2S TX PCM-to-PDM conversion. (R/W)
```

```markdown
Register 29.9. I2S_TX_PCM2PDM_CONF1_REG (0x0044)

| Bit | Description |
|-----|-------------|
| 31  | reserved   |
| 20  | I2S_TX_PDM_FS |
| 19  |             |
| 10  | 9          |
| 0   | Reset      |

I2S_TX_PDM_FS I2S PDM TX upsampling parameter. (R/W)
```