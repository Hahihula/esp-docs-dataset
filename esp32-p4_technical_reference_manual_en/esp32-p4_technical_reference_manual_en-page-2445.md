

```markdown
Register 45.4. ANA_I2C_MST_I2CO_CTRL1_REG (0x0024)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 11-10|                                     |
|     | Ox1                                                                          |
|     | Ox2                                                                          |
|     | Reset                                                                        |

ANA_I2C_MST_I2CO_SCL_PULSE_DUR Configures the duration of the high-level period of the SCL driven by I2CO. The duration is measured by the counter operating on the LP_FAST_CLK clock. (R/W)

ANA_I2C_MST_I2CO_SDA_SIDE_GUARD Configures the duration of the low-level period of the SCL driven by I2CO. The duration is measured by the counter operating on the LP_FAST_CLK clock. (R/W)


Register 45.5. ANA_I2C_MST_I2C1_CTRL1_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 11-10|                                     |
|     | Ox1                                                                          |
|     | Ox2                                                                          |
|     | Reset                                                                        |

ANA_I2C_MST_I2C1_SCL_PULSE_DUR Configures the duration of the high-level period of the SCL driven by I2C1. The duration is measured by the counter operating on the LP_FAST_CLK clock. (R/W)

ANA_I2C_MST_I2C1_SDA_SIDE_GUARD Configures the duration of the low-level period of the SCL driven by I2C1. The duration is measured by the counter operating on the LP_FAST_CLK clock. (R/W)
```