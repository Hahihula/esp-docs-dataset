

```markdown
Register 8.43. LP_GPIO_OUT_REG (0x0004)

LP_GPIO_OUT_DATA_ORIG Configures the output of GPIO0~GPIO6.

The value of each bit can be:
O: Low level
1: High level
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(R/W/WTC)
```

```markdown
Register 8.44. LP_GPIO_OUT_W1TS_REG (0x0008)

LP_GPIO_OUT_W1TS Configures whether or not to enable the output register LP_IO_OUT_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_OUT_REG will be set to 1
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to set LP_GPIO_OUT_REG.
(WT)
```