

```markdown
Register 6.49. LP_GPIO_STATUS_W1TC_REG (0x0028)

LP_GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register LP_GPIO_STATUS_INT of GPIO0~GPIO6.

The value of each bit can be:
O: Not clear
1: The corresponding bit in LP_GPIO_STATUS_INT will be cleared
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to clear LP_GPIO_STATUS_INT. (WT)

Register 6.50. LP_GPIO_STATUS_NEXT_REG (0x002C)

LP_GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source status of GPIO0~GPIO6.
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Each bit represents:
O: Interrupt source status is invalid.
1: Interrupt source status is valid.
The interrupt here can be rising-edge triggered, falling-edge triggered, any edge triggered, or level triggered. (RO)
```