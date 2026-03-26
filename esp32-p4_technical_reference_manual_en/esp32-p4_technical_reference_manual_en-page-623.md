

```markdown
Register 9.69. LP_GPIO_ENABLE_REG (0x0014)

LP_GPIO_ENABLE_DATA Configures whether or not to enable the output of GPIO0 ~ GPIO15.
O: Not enable
1: Enable
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid.
(R/W/WTC)
```

```markdown
Register 9.70. LP_GPIO_ENABLE_W1TS_REG (0x0018)

LP_GPIO_ENABLE_DATA_W1TS Configures whether or not to set the output enable register LP_GPIO_ENABLE_REG of GPIO0 ~ GPIO15.
O: Not set
1: The corresponding bit in LP_GPIO_ENABLE_REG will be set to 1
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid. Recommended operation: use this register to set LP_GPIO_ENABLE_REG.
(WT)
```