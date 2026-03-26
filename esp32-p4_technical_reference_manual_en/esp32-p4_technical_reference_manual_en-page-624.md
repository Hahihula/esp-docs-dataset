

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.71. LP_GPIO_ENABLE_W1TC_REG (0x001C)

LP_GPIO_ENABLE_DATA_W1TC Configures whether or not to clear the output enable register LP_GPIO_ENABLE_REG of GPIO0 ~ GPIO15.

O: Not clear
1: The corresponding bit in LP_GPIO_ENABLE_REG will be cleared

Bit0 ~ bit15 are corresponding to GPIO0 ~ 15. Bit16 ~ bit31 are invalid. Recommended operation: use this register to clear LP_GPIO_ENABLE_REG.
(WT)

Register 9.72. LP_GPIO_STATUS_REG (0x0020)

LP_GPIO_STATUS_DATA The interrupt status of GPIO0 ~ GPIO15, can be configured by the software.

Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid.
Each bit represents the status of its corresponding GPIO:

O: Represents the GPIO does not generate the interrupt configured by LP_GPIO_PINn_INT_TYPE, or this bit is configured to 0 by the software.

1: Represents the GPIO generates the interrupt configured by LP_GPIO_PINn_INT_TYPE, or this bit is configured to 1 by the software.
(R/W/WTC)
```