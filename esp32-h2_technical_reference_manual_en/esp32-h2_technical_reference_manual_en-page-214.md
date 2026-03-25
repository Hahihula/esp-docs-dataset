

```markdown
Register 5.112. EFUSE_RD_TIM_CONF_REG (0x01EC)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----:|----:|----:|----:|---|---|---|
| 0x12 | 0x1 |     |    | 0x2 |   |   | 0x1 |

EFUSE_THR_A Configures the read hold time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_TRD Configures the read time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_TSUR_A Configures the read setup time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_READ_INIT_NUM Configures the waiting time of reading eFuse memory. Measurement unit: One cycle of the eFuse core clock. (R/W)
```

```markdown
Register 5.113. EFUSE_WR_TIM_CONF1_REG (0x01FO)

| 31 | 24 | 23 | 8 | 7 | 0 |
|-----|----:|----:|---|---|---|
| 0x1 |     |     |   |   | 0x1 |

EFUSE_TSUP_A Configures the programming setup time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_PWR_ON_NUM Configures the power up time for VDDQ. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_THP_A Configures the programming hold time. Measurement unit: One cycle of the eFuse core clock. (R/W)
```