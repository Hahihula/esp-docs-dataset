

```markdown
## Register 9.75. LP_GPIO_STATUS_NEXT_REG (0x002C)

LP_GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source signal of GPIO0 ~ GPIO15.
Bit0 ~ bit15 are corresponding to GPIO0 ~ 15. Bit16 ~ bit31 are invalid. Each bit represents:
O: The GPIO does not generate the interrupt configured by LP_GPIO_PINn_INT_TYPE.
1: The GPIO generates an interrupt configured by LP_GPIO_PINn_INT_TYPE.
The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt.
(RO)

## Register 9.76. LP_GPIO_IN_REG (0x0030)

LP_GPIO_IN_DATA_NEXT Represents the input value of GPIO0 ~ GPIO15. Each bit represents a pin
input value:
O: Low level
1: High level.
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid.
(RO)
```