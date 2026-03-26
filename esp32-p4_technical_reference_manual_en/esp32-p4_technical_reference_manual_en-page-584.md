

```markdown
Register 9.11. GPIO_ENABLE1_W1TS_REG (0x0030)

| 31 | 25 | 24 | ... | 0 |
|----:|----:|----:|-----|---|
|    |    |    |     | Reset |
| 0  | 0  | 0  | 0   | 0x00000 |

GPIO_ENABLE1_W1TS Configures whether or not to set the output enable register GPIO_ENABLE1_REG of GPIO32 ~ GPIO54.
O: Not set
1: The corresponding bit in GPIO_ENABLE1_REG will be set to 1
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. Recommended operation: use this register to set GPIO_ENABLE1_REG.
(WT)

Register 9.12. GPIO_ENABLE1_W1TC_REG (0x0034)

| 31 | 25 | 24 | ... | 0 |
|----:|----:|----:|-----|---|
|    |    |    |     | Reset |
| 0  | 0  | 0  | 0   | 0x00000 |

GPIO_ENABLE1_W1TC Configures whether or not to clear the output enable register GPIO_ENABLE1_REG of GPIO32 ~ GPIO54.
O: Not clear
1: The corresponding bit in GPIO_ENABLE1_REG will be cleared
Bit0 ~ bit22 are corresponding to GPIO32 ~ 54. Recommended operation: use this register to clear GPIO_ENABLE1_REG.
(WT)
```