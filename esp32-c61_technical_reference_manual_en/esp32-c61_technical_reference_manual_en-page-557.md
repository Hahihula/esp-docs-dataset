

```markdown
Register 11.49. PMU_LP_SLEEP_BIAS_REG (0x00C8)

| Bit | 31 | 30 | 29       | 28           | 27             | ... | 0 |
|-----|----|----|----------|--------------|----------------|-----|---|
|     | PMU_LP_SLEEP_BIAS_SLEEP | PMU_LP_SLEEP_PD_CUR | PMU_LP_SLEEP_XPD_BIAS | PMU_LP_SLEEP_DBG_ATTEN | (reserved) | ... | Reset |

PMU_LP_SLEEP_XPD_BIAS Configures the power supply of BIAS in LP_SLEEP state. (R/W)

PMU_LP_SLEEP_DBG_ATTEN Configures the degree of attenuation of the analog band gap in LP_SLEEP state. (R/W)

PMU_LP_SLEEP_PD_CUR Configures the power-down current in LP_SLEEP state. (R/W)

PMU_LP_SLEEP_BIAS_SLEEP Configures the sleep or wakeup status of the BIAS circuit in LP_SLEEP state. (R/W)
```