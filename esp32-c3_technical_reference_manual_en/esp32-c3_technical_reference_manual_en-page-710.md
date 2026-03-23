

```markdown
## 28.8 Registers

The addresses in this section are relative to I2C Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 28.1. I2C_SCL_LOW_PERIOD_REG (0x0000)

I2C_SCL_LOW_PERIOD This field is used to configure how long SCL remains low in master mode, in I2C module clock cycles. (R/W)

Register 28.2. I2C_SDA_HOLD_REG (0x0030)

I2C_SDA_HOLD_TIME This field is used to configure the time to hold the data after the falling edge of SCL, in I2C module clock cycles. (R/W)

Register 28.3. I2C_SDA_SAMPLE_REG (0x0034)

I2C_SDA_SAMPLE_TIME This field is used to configure how long SDA is sampled, in I2C module clock cycles. (R/W)
```