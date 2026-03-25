

```markdown
Register 31.7. I2S_TX_PCM2PDM_CONF_REG (0x0040)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | 1  | 0  | Ox1| Ox1| Ox1| Ox1| Ox1| Ox1| Ox1| (reserved)| I2S_TX_PDM_SINC_OSR2 | (reserved) |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Ox1| Ox1|    |    |    |    |    |    |    |    |          |             |            |
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset|      |      |      |      |      |      |      |          |             |            |

I2S_TX_PDM_SINC_OSR2 Configures I2S TX PDM OSR value. (R/W)

I2S_TX_PDM_DAC_2OUT_EN Configures DAC output mode.
O: Enable 1-line DAC output mode
1: Enable 2-line DAC output mode
Only valid when I2S_TX_PDM_DAC_MODE_EN is set.
(R/W)

I2S_TX_PDM_DAC_MODE_EN Configures whether to enable 1-line PDM output mode or DAC output mode.
O: Enable 1-line PDM output mode
1: Enable DAC output mode
(R/W)

I2S_PCM2PDM_CONV_EN Configures whether to enable I2S TX PCM-to-PDM conversion.
O: Disable
1: Enable
(R/W)

Register 31.8. I2S_TX_PCM2PDM_CONF1_REG (0x0044)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | 7  | 7  | (reserved)| I2S_TX_PDM_FS | (reserved) | (reserved) |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 7  | 7  | 480| 960|      | Reset|          |

I2S_TX_PDM_FS Configures I2S PDM TX upsampling parameter. (R/W)
```