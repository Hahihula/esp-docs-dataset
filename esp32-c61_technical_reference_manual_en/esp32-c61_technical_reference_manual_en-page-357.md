

```markdown
Register 7.27. PCR_I2S_RX_CLKM_DIV_CONF_REG (0x0070)

| 31 | 28 | 27 | 26 | 18 | 17 | 9 | 8 | 0 |
|-----|----:|----:|----:|----:|----:|---:|---:|---:|
| 0   |  0 |  0 |  0 |    |    |   |   | Reset |

PCR_I2S_RX_CLKM_DIV_Z  For b <= a/2, the value of I2S_RX_CLKM_DIV_Z is b. For b > a/2, the value of I2S_RX_CLKM_DIV_Z is (a-b). (R/W)

PCR_I2S_RX_CLKM_DIV_Y  For b <= a/2, the value of I2S_RX_CLKM_DIV_Y is (a%b) . For b > a/2, the value of I2S_RX_CLKM_DIV_Y is (a%(a-b)). (R/W)

PCR_I2S_RX_CLKM_DIV_X  For b <= a/2, the value of I2S_RX_CLKM_DIV_X is (a/b) - 1. For b > a/2, the value of I2S_RX_CLKM_DIV_X is (a/(a-b)) - 1. (R/W)

PCR_I2S_RX_CLKM_DIV_YN1 For b <= a/2, the value of I2S_RX_CLKM_DIV_YN1 is 0 . For b > a/2, the value of I2S_RX_CLKM_DIV_YN1 is 1. (R/W)


Register 7.28. PCR_SARADC_CONF_REG (0x0074)

| 31 |     |     | ... | 4 | 3 | 2 | 1 | 0 |
|-----|-----|-----|-----|---:|---:|---:|---:|---:|
| 0   |  0  |  0  |  0  |  0 |  0 |  0 |  1 |  1 | Reset |

PCR_SARADC_RST_EN Configures whether or not to reset functional registers of SAR ADC.
O: Not reset
1: Reset
(R/W)

PCR_SARADC_REG_CLK_EN Configures whether or not to enable APB_CLK for SAR ADC.
O: Not enable
1: Enable
(R/W)

PCR_SARADC_REG_RST_EN Configures whether or not to reset APB registers of SAR ADC.
O: Not reset
1: Reset
(R/W)
```