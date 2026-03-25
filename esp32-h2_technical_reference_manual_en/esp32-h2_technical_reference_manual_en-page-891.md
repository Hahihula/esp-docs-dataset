

```markdown
Register 30.26. I2C_COMD1_REG (0x005C)

| 31 | 30 | ... | 14 | 13 | ... | 0 |
|----|----|-----|----|----|-----|---|
| 0  | 0  | 0   | 0  | 0  | 0   | 0 |

I2C_COMMAND1 Configures command 1. See details in I2C_COMDO_REG. (R/W)

I2C_COMMAND1_DONE Represents whether command 1 is done in I2C Master mode.
O: Not done
1: Done
(R/W/SS)
```

```markdown
Register 30.27. I2C_COMD2_REG (0x0060)

| 31 | 30 | ... | 14 | 13 | ... | 0 |
|----|----|-----|----|----|-----|---|
| 0  | 0  | 0   | 0  | 0  | 0   | 0 |

I2C_COMMAND2 Configures command 2. See details in I2C_COMDO_REG. (R/W)

I2C_COMMAND2_DONE Represents whether command 2 is done in I2C Master mode.
O: Not done
1: Done
(R/W/SS)
```