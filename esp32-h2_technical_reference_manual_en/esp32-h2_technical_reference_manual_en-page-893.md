

```markdown
Register 30.30. I2C_COMD5_REG (0x006C)

| Bit | Description                |
|-----|----------------------------|
| 31:30 | (reserved)               |
| 14:0   | I2C_COMMAND5             |

I2C_COMMAND5 Configures command 5. See details in I2C_COMDO_REG. (R/W)
I2C_COMMAND5_DONE Represents whether command 5 is done in I2C Master mode.
O: Not done
1: Done
(R/W/SS)

Register 30.31. I2C_COMD6_REG (0x0070)

| Bit | Description                |
|-----|----------------------------|
| 31:30 | (reserved)               |
| 14:0   | I2C_COMMAND6             |

I2C_COMMAND6 Configures command 6. See details in I2C_COMDO_REG. (R/W)
I2C_COMMAND6_DONE Represents whether command 6 is done in I2C Master mode.
O: Not done
1: Done
(R/W/SS)
```