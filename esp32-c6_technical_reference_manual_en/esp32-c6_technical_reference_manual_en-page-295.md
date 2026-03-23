

```markdown
Register 7.35. LP_IO_OUT_REG (0x0000)

LP_GPIO_OUT_DATA Configures the output of GPIO0 ~ GPIO7.
O: Low level
1: High level
bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
(R/W)
```

```markdown
Register 7.36. LP_IO_OUT_W1TS_REG (0x0004)

LP_GPIO_OUT_DATA_W1TS Configures whether or not to enable the output register LP_IO_OUT_REG of GPIO0 ~ GPIO7.

- bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
- If the value 1 is written to a bit here, the corresponding bit in LP_IO_OUT_REG will be set to 1.
- Recommended operation: use this register to set LP_IO_OUT_REG.
(WT)
```