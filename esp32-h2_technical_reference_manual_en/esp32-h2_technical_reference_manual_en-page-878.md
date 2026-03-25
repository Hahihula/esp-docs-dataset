

```markdown
Register 30.12. I2C_TO_REG (0x000C)

| Bit | Description                  |
|-----|------------------------------|
| 6   | I2C_TIME_OUT_EN             |
| 5   | I2C_TIME_OUT_VALUE          |
| ... | (reserved)                   |
| 0   | Reset                       |

I2C_TIME_OUT_VALUE Configures the timeout threshold period for SCL sticking at the high or low level. The actual period is `2^I2C_TIME_OUT_VALUE`.
Measurement unit: I2C_SCLK
(R/W)

I2C_TIME_OUT_EN Configures whether to enable timeout control.
0: No effect
1: Enable
(R/W)
```

```markdown
Register 30.13. I2C_SLAVE_ADDR_REG (0x0010)

| Bit | Description                  |
|-----|------------------------------|
| 15  | I2C_SLAVE_ADDR              |
| ... | (reserved)                   |
| 0   | Reset                       |

I2C_SLAVE_ADDR Configures the slave address of the I2C slave.
(R/W)

I2C_ADDR_10BIT_EN Configures whether to enable the slave 10-bit addressing mode in Master mode.
0: No effect
1: Enable
(R/W)
```