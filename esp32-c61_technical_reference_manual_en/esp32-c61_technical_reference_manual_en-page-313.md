

```markdown
Register 6.43. LP_GPIO_ENABLE_REG (0x0010)

LP_GPIO_ENABLE_DATA   Configures whether or not to enable the output of GPIO0~GPIO6.
The value of each bit can be:
O: Not enable
1: Enable
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(R/W/WTC)
```

```markdown
Register 6.44. LP_GPIO_ENABLE_W1TS_REG (0x0014)

LP_GPIO_ENABLE_W1TS   Configures whether or not to set the output enable register
LP_GPIO_ENABLE_REG of GPIO0~GPIO6.
The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_ENABLE_REG will be set to 1
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to set LP_GPIO_ENABLE_REG.
(WT)
```