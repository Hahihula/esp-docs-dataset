

```markdown
Register 6.41. LP_GPIO_OUT_W1TS_REG (0x0008)

LP_GPIO_OUT_W1TS Configures whether or not to enable the output register LP_GPIO_OUT_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_OUT_REG will be set to 1
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to set LP_GPIO_OUT_REG. (WT)

Register 6.42. LP_GPIO_OUT_W1TC_REG (0x000C)

LP_GPIO_OUT_W1TC Configures whether or not to clear the output register LP_GPIO_OUT_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_OUT_REG will be cleared.
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to clear LP_GPIO_OUT_REG. (WT)
```