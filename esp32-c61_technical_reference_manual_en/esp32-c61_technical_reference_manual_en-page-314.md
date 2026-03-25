

```markdown
Register 6.45. LP_GPIO_ENABLE_W1TC_REG (0x0018)

LP_GPIO_ENABLE_W1TC   Configures whether or not to clear the output enable register LP_GPIO_ENABLE_REG of GPIO0~GPIO6.
The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_ENABLE_REG will be cleared
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.

Recommended operation: use this register to clear LP_GPIO_ENABLE_REG.
(WT)

Register 6.46. LP_GPIO_IN_REG (0x001C)

LP_GPIO_IN_DATA_NEXT   Represents the input value of GPIO0~GPIO6.
Each bit represents a pin input value:
O: Low level input
1: High level input
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(RO)
```