

```markdown
Register 28.4. I2C_SCL_HIGH_PERIOD_REG (0x0038)

I2C_SCL_HIGH_PERIOD This field is used to configure how long SCL remains high in master mode, in I2C module clock cycles. (R/W)

I2C_SCL_WAIT_HIGH_PERIOD This field is used to configure the SCL_FSM's waiting period for SCL high level in master mode, in I2C module clock cycles. (R/W)


Register 28.5. I2C_SCL_START_HOLD_REG (0x0040)

I2C_SCL_START_HOLD_TIME This field is used to configure the time between the falling edge of SDA and the falling edge of SCL for a START condition, in I2C module clock cycles. (R/W)


Register 28.6. I2C_SCL_RSTART_SETUP_REG (0x0044)

I2C_SCL_RSTART_SETUP_TIME This field is used to configure the time between the rising edge of SCL and the falling edge of SDA for a RSTART condition, in I2C module clock cycles. (R/W)
```