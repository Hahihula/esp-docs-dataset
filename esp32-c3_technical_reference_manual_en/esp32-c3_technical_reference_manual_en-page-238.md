

```markdown
Register 9.11. RTC_CNTL_ANA_CONF_REG (0x0034)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | RTC_CNTL_PLL_I2C_PU (reserved) | RTC_CNTL_CKGEN_I2C_PU (reserved) | RTC_CNTL_RFRX_PBUS_PU (reserved) | RTC_CNTL_TXRF_I2C_PU (reserved) | RTC_CNTL_SAR_I2C_PU (reserved) | RTC_CNTL_GLITCH_RST_EN | RTC_CNTL_RESET_POR_FORCE_PD | RTC_CNTL_RESET_POR_FORCE_PU | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 |

RTC_CNTL_RESET_POR_FORCE_PD    Set this bit to force not bypass I2C power-on reset. (R/W)
RTC_CNTL_RESET_POR_FORCE_PU     Set this bit to force bypass I2C power-on reset. (R/W)
RTC_CNTL_GLITCH_RST_EN          Set this bit to enable reset when the system detects a glitch. (R/W)
RTC_CNTL_SAR_I2C_PU             Set this bit to FPU the SAR_I2C. (R/W)
RTC_CNTL_TXRF_I2C_PU            Set this bit to PU TXRF_I2C. (R/W)
RTC_CNTL_RFRX_PBUS_PU           Set this bit to PU RFRX_PBUS. (R/W)
RTC_CNTL_CKGEN_I2C_PU           Set this bit to PU CKGEN_I2C. (R/W)
RTC_CNTL_PLL_I2C_PU             Set this bit to PU PLL I2C. (R/W)
```