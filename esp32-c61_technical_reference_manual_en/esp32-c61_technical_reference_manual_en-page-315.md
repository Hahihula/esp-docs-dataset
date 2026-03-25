

```markdown
Register 6.47. LP_GPIO_STATUS_REG (0x0020)

LP_GPIO_STATUS_INTERRUPT Configures the interrupt status of GPIO0~GPIO6.

The value of each bit can be:
O: No interrupt
1: Interrupt is triggered
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
This field is used together with LP_GPIO_PINn_INT_TYPE in register LP_GPIO_PINn_REG.
(R/W/WTC)

Register 6.48. LP_GPIO_STATUS_W1TS_REG (0x0024)

LP_GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register
LP_GPIO_STATUS_INT of GPIO0~GPIO6.

The value of each bit can be:
O: Not set
1: The corresponding bit in LP_GPIO_STATUS_INT will be set
Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.
Recommended operation: use this register to set LP_GPIO_STATUS_INT.
(WT)
```