

```markdown
Register 9.67. LP_GPIO_OUT_W1TS_REG (0x000C)

LP_GPIO_OUT_DATA_W1TS Configures whether or not to set the output register LP_GPIO_OUT_REG of GPIO0 ~ GPIO15.
0: Not set
1: The corresponding bit in LP_GPIO_OUT_REG will be set to 1
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid. Recommended operation: use this register to set LP_GPIO_OUT_REG. (WT)

Register 9.68. LP_GPIO_OUT_W1TC_REG (0x0010)

LP_GPIO_OUT_DATA_W1TC Configures whether or not to clear the output register LP_GPIO_OUT_REG of GPIO0 ~ GPIO15 output.
0: Not clear
1: The corresponding bit in LP_GPIO_OUT_REG will be cleared.
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid. Recommended operation: use this register to clear LP_GPIO_OUT_REG. (WT)
```