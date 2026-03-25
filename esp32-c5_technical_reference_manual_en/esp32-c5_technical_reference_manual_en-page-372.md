

```markdown
Register 8.45. LP_GPIO_OUT_W1TC_REG (0x000C)

LP_GPIO_OUT_W1TC Configures whether or not to clear the output register LP_GPIO_OUT_REG of GPIO0~GPIO6.

The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_OUT_REG will be cleared.
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.

Recommended operation: use this register to clear LP_GPIO_OUT_REG.
(WT)

Register 8.46. LP_GPIO_ENABLE_REG (0x0010)

LP_GPIO_ENABLE_DATA Configures whether or not to enable the output of GPIO0~GPIO6.

The value of each bit can be:
O: Not enable
1: Enable
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(R/W/WT/C)
```