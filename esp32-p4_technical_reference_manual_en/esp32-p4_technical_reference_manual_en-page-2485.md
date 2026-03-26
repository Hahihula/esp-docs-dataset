

```markdown
Register 46.12. I2S_TX_PCM2PDM_CONF_REG (for I2S0 only) (0x0040)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | (reserved)                      |
| 30  | I2S_TX_PDM_SINC_OSR2            |
| 29  | I2S_PCM2PDM_CONV_EN             |
| 28  | I2S_TX_PDM_DAC_MODE_EN          |
| 27  | I2S_TX_PDM_DAC_2OUT_EN          |
| 26  | (reserved)                      |
| 25  | (reserved)                      |
| 24  | (reserved)                      |
| 23  | (reserved)                      |
| 22  | (reserved)                      |
| 21  | (reserved)                      |
| 20  | (reserved)                      |
| 19  | I2S_TX_PDM_SINC_OSR2            |
| 18  | DAC_MODE_EN                     |
| 17  | DAC_2OUT_EN                     |
| 16  | (reserved)                      |
| 15  | (reserved)                      |
| 14  | (reserved)                      |
| 13  | (reserved)                      |
| 12  | (reserved)                      |
| 11  | I2S_TX_PDM_SINC_OSR2            |
| 10  | Reset                           |
| 9   | 0x2                             |
| 8   | 0                               |

I2S_TX_PDM_SINC_OSR2 Configures I2S TX PDM OSR value. (R/W)

I2S_TX_PDM_DAC_2OUT_EN Configures whether to enable I2S TX PDM DAC mode.
O: Enable 1-line DAC output mode
1: Enable 2-line DAC output mode
Only valid when I2S_TX_PDM_DAC_MODE_EN is set.
(R/W)

I2S_TX_PDM_DAC_MODE_EN Configures whether to enable 1-line PDM output mode or DAC output mode.
O: Enable 1-line PDM output mode
1: Enable DAC output mode
(R/W)

I2S_PCM2PDM_CONV_EN Configures whether to enable the I2S TX PCM-to-PDM converter.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 46.13. I2S_TX_PCM2PDM_CONF1_REG (0x0044)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | (reserved)                      |
| 30  | (reserved)                      |
| 29  | (reserved)                      |
| 28  | I2S_TX_PDM_FP                   |
| 27  | (reserved)                      |
| 26  | (reserved)                      |
| 25  | (reserved)                      |
| 24  | (reserved)                      |
| 23  | (reserved)                      |
| 22  | (reserved)                      |
| 21  | (reserved)                      |
| 20  | (reserved)                      |
| 19  | (reserved)                      |
| 18  | (reserved)                      |
| 17  | (reserved)                      |
| 16  | (reserved)                      |
| 15  | (reserved)                      |
| 14  | (reserved)                      |
| 13  | (reserved)                      |
| 12  | (reserved)                      |
| 11  | I2S_TX_PDM_FS                   |
| 10  | Reset                           |
| 9   | 960                             |
| 8   | 7                               |

I2S_TX_PDM_FS Configures I2S PDM TX upsampling parameter. (R/W)
```