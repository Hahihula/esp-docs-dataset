

```markdown
## Register 5.114. EFUSE_WR_TIM_CONF2_REG (0x01F4)

| Bit Range | Description |
|-----------|-------------|
| 31        |             |
|           | EFUSE_PWR_OFF_NUM Configures the power outage time for VDDQ. Measurement unit: One cycle of the eFuse core clock. (R/W) |
| 16-15     |             |
|           | EFUSE_TPGM Configures the active programming time. Measurement unit: One cycle of the eFuse core clock. (R/W) |

## Register 5.115. EFUSE_WR_TIM_CONF0_REG (0x01F8)

| Bit Range | Description |
|-----------|-------------|
| 31        |             |
|           | (reserved) |
| 21-20     |             |
|           | EFUSE_TPGM_INACTIVE Configures the inactive programming time. Measurement unit: One cycle of the eFuse core clock. (R/W) |
| 19-18     |             |
|           | (reserved) |
| 17        |             |
|           | EFUSE_UPDATE Configures whether to update multi-bit register signals.<br>1: Update<br>0: No effect (WT) |
| 16-12     |             |
|           | (reserved) |

## Register 5.116. EFUSE_DATE_REG (0x01FC)

| Bit Range | Description |
|-----------|-------------|
| 31        |             |
|           | (reserved) |
| 28-27     |             |
|           | EFUSE_DATE Version control register. (R/W) |

```
*Note: The diagrams represent register bit fields with labels indicating the purpose of each segment or field, such as `EFUSE_PWR_OFF_NUM`, `EFUSE_TPGM`, and their respective positions within the 32-bit registers.*