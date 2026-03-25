

```markdown
Chapter 27 I2C Controller (I2C)
GoBack

Register 27.12. I2C_TO_REG (0x000C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| ... | ...                          |
| 6   |                              |
| 5   |                              |
| 4   |                              |
| 0   | Reset                        |

I2C_TIME_OUT_VALUE Configures the timeout threshold period for SCL stuck at high or low level.
The actual period is 2^(I2C_TIME_OUT_VALUE+1)-1.
Measurement unit: I2C_SCLK clock cycles
(R/W)

I2C_TIME_OUT_EN Configures to enable time out control.
0: No effect
1: Enable
(R/W)

Register 27.13. I2C_SLAVE_ADDR_REG (0x0010)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| ... | ...                          |
| 15  |                              |
| 14  |                              |
| 0   | Reset                        |

I2C_SLAVE_ADDR Configure the slave address of I2C Slave.
(R/W)

I2C_ADDR_10BIT_EN Configures to enable the slave 10-bit addressing mode in master mode.
0: No effect
1: Enable
(R/W)
```