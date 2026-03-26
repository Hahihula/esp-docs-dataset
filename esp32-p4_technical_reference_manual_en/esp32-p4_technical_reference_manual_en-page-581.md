

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.5. GPIO_OUT1_W1TS_REG (0x0014)

| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| 25  |                     |
| 24  |                     |
|     |                     |
| 0   |                     |

GPIO_OUT1_W1TS Configures whether or not to set the output register GPIO_OUT1_REG of GPIO32 ~ GPIO54.
O: Not set
1: The corresponding bit in GPIO_OUT1_REG will be set to 1
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. Recommended operation: use this register to set GPIO_OUT1_REG.
(WT)

Register 9.6. GPIO_OUT1_W1TC_REG (0x0018)

| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| 25  |                     |
| 24  |                     |
|     |                     |
| 0   |                     |

GPIO_OUT1_W1TC Configures whether or not to clear the output register GPIO_OUT1_REG of GPIO32 ~ GPIO54 output.
O: Not clear
1: The corresponding bit in GPIO_OUT1_REG will be cleared.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. Recommended operation: use this register to clear GPIO_OUT_REG.
(WT)
```