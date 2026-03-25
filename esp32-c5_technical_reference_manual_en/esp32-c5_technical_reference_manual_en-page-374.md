

```markdown
Chapter 8 GPIO Matrix and IO MUX

Register 8.49. LP_GPIO_IN_REG (0x001C)

LP_GPIO_IN_DATA_NEXT Represents the input value of GPIO0~GPIO6.
Each bit represents a pin input value:
O: Low level input
1: High level input
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
(RO)

Register 8.50. LP_GPIO_STATUS_REG (0x0020)

LP_GPIO_STATUS_INTERRUPT Configures the interrupt status of GPIO0~GPIO6.
The value of each bit can be:
O: No interrupt
1: Interrupt is triggered
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
This field is used together with LP_GPIO_PINn_INT_TYPE in register LP_GPIO_PINn_REG.
(R/W/WTC)
```