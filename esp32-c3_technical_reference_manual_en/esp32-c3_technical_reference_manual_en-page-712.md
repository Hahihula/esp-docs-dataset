

```markdown
Register 28.7. I2C_SCL_STOP_HOLD_REG (0x0048)

I2C_SCL_STOP_HOLD_TIME This field is used to configure the delay after the STOP condition, in I2C module clock cycles. (R/W)

Register 28.8. I2C_SCL_STOP_SETUP_REG (0x004C)

I2C_SCL_STOP_SETUP_TIME This field is used to configure the time between the rising edge of SCL and the rising edge of SDA, in I2C module clock cycles. (R/W)

Register 28.9. I2C_SCL_ST_TIME_OUT_REG (0x0078)

I2C_SCL_ST_TO_I2C The maximum time that SCL FSM remains unchanged. It should be no more than 23. (R/W)
```