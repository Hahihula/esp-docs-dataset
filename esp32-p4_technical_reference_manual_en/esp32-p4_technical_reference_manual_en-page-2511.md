

```markdown
Register 47.6. LP_I2S_RX_PDM_CONF_REG (0x0070)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | (reserved) | LP_I2S_RX_PDM_HP_BYPASS | LP_I2S_RX_PDM_PDM2PCM_AMPLIFY_NUM | LP_I2S_RX_PDM_SINC_DSR_16_EN | LP_I2S_RX_PDM2PCM_EN |    |    |    |    |    |    |
|     | 0x7 | 0x6 | 0   | 0x1 | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |

LP_I2S_RX_PDM2PCM_EN Configures whether to enable the PDM-to-PCM converter in RX mode.
O: Disable
1: Enable
(R/W)

LP_I2S_RX_PDM_SINC_DSR_16_EN Configures the downsampling rate of PDM RX filter group 1 module.
O: 64
1: 128
(R/W)

LP_I2S_RX_PDM2PCM_AMPLIFY_NUM Configures the PDM-to-PCM RX amplification coefficient. PCM data will be multiplied by this value before outputting. (R/W)

LP_I2S_RX_PDM_HP_BYPASS Configures whether PDM-to-PCM RX bypasses the HP filter.
O: Not bypass
1: Bypass
(R/W)
```