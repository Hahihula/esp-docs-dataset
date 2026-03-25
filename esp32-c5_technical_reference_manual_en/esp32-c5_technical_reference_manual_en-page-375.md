

```markdown
Chapter 8 GPIO Matrix and IO MUX

Register 8.51. LP_GPIO_STATUS_W1TS_REG (0x0024)

LP_GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register LP_GPIO_STATUS_INT of GPIO0~GPIO6.

The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_STATUS_INT will be set
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.

Recommended operation: use this register to set LP_GPIO_STATUS_INT.
(WT)

Register 8.52. LP_GPIO_STATUS_W1TC_REG (0x0028)

LP_GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register LP_GPIO_STATUS_INT of GPIO0~GPIO6.

The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_STATUS_INT will be cleared
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.

Recommended operation: use this register to clear LP_GPIO_STATUS_INT.
(WT)
```