

```markdown
Register 8.47. LP_GPIO_ENABLE_W1TS_REG (0x0014)

LP_GPIO_ENABLE_W1TS Configures whether or not to set the output enable register LP_GPIO_ENABLE_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_ENABLE_REG will be set to 1
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to set LP_GPIO_ENABLE_REG.
(WT)

Register 8.48. LP_GPIO_ENABLE_W1TC_REG (0x0018)

LP_GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register LP_GPIO_ENABLE_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_ENABLE_REG will be cleared.
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to clear LP_GPIO_ENABLE_REG.
(WT)
```