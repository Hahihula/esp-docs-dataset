

```markdown
Register 7.36. EFUSE_WR_TIM_CONF1_REG (0x01F4)

| 31 | 24 | 23 | ... | 8 | 7 | ... | 0 |
|-----|-----|-----|-----|----|---|-----|---|
|     |     |     |     |    |   |     |   |
| 0x1 |     |     |     |    |   |     |   |
|     |     |     |     |    |   |     | Reset |

EFUSE_TSUP_A Configures the programming setup time. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_PWR_ON_NUM Configures the power up time for VDDQ. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_THP_A Configures the programming hold time. Measurement unit: One cycle of the eFuse core clock. (R/W)
```

```markdown
Register 7.37. EFUSE_WR_TIM_CONF2_REG (0x01F4)

| 31 | 16 | 15 | ... | 0 |
|-----|-----|-----|-----|---|
|     |     |     |     |   |
| 0xc8 |     |     |     |   |
|     |     |     |     | Reset |

EFUSE_PWR_OFF_NUM Configures the power outage time for VDDQ. Measurement unit: One cycle of the eFuse core clock. (R/W)

EFUSE_TPGM Configures the active programming time. Measurement unit: One cycle of the eFuse core clock. (R/W)
```