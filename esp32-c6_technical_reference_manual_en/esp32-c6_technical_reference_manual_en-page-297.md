

```markdown
Register 7.39. LP_IO_ENABLE_W1TS_REG (0x0010)

LP_GPIO_ENABLE_W1TS Configures whether or not to set the output enable register LP_IO_ENABLE_REG of GPIO0 ~ GPIO7.
- bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
- If the value 1 is written to a bit here, the corresponding bit in LP_IO_ENABLE_REG will be set to 1.
- Recommended operation: use this register to set LP_IO_ENABLE_REG.

(WT)

Register 7.40. LP_IO_ENABLE_W1TC_REG (0x0014)

LP_GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register LP_IO_ENABLE_REG of GPIO0 ~ GPIO7.
- bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
- If the value 1 is written to a bit here, the corresponding bit in LP_IO_ENABLE_REG will be cleared.
- Recommended operation: use this register to clear LP_IO_ENABLE_REG.

(WT)
```