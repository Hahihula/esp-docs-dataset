

```markdown
Register 11.7. PMU_HP_ACTIVE_BIAS_REG (0x0018)

| Bit | 31 | 30 | 29 | 26 | 25 | 24 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     |    | PMU_HP_ACTIVE_BIAS_SLEEP | PMU_HP_ACTIVE_XPD_BIAS | PMU_HP_ACTIVE_DBG_ATTEN | reserved | Reset |

PMU_HP_ACTIVE_XPD_BIAS Configures the power supply of BIAS in HP_ACTIVE state. (R/W)

PMU_HP_ACTIVE_DBG_ATTEN Configures the degree of attenuation of the analog band gap in HP_ACTIVE state. (R/W)

PMU_HP_ACTIVE_PD_CUR Configures the power-down current in HP_ACTIVE state. (R/W)

PMU_HP_ACTIVE_BIAS_SLEEP Configures the sleep or wakeup status of the BIAS circuit in HP_ACTIVE state. (R/W)
```