

```markdown
Register 10.79. LPPERI_LP_I2S_RXCLK_DIV_XYZ_REG (0x0034)

| 31 | 23 | 22 | 14 | 13 | 5 | 4 | 3 | 0 |
|-----|-----|-----|----|----|---|---|---|---|
| 0x0 |     | Ox1 |    |    |   |   |   | Reset |

LPPERI_LP_I2S_RX_CLKM_DIV_YN1 Configures the yn1 coefficient of the LP I2S RX clock divisor. (R/W)

LPPERI_LP_I2S_RX_CLKM_DIV_Z Configures the z coefficient of the LP I2S RX clock divisor. (R/W)

LPPERI_LP_I2S_RX_CLKM_DIV_Y Configures the y coefficient of the LP I2S RX clock divisor. (R/W)

LPPERI_LP_I2S_RX_CLKM_DIV_X Configures the x coefficient of the LP I2S RX clock divisor. (R/W)


Register 10.80. LPPERI_DATE_REG (0x03FC)

| 31 | 30 |
|-----|-----|
|     | Reset |

LPPERI_CLK_EN Configures resister clock gating.
0: Support clock only when application writes registers
1: Force on clock gating for registers
(R/W)
```