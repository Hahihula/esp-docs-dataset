

```markdown
Register 9.73. LP_GPIO_STATUS_W1TS_REG (0x0024)

LP_GPIO_STATUS_DATA_W1TS Configures whether or not to set the interrupt status register LP_GPIO_STATUS_DATA of GPIO0 ~ GPIO15.
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid.
If the value 1 is written to a bit here, the corresponding bit in LP_GPIO_STATUS_DATA will be set to 1.

Recommended operation: use this register to set LP_GPIO_STATUS_DATA.
(WT)

Register 9.74. LP_GPIO_STATUS_W1TC_REG (0x0028)

LP_GPIO_STATUS_DATA_W1TC Configures whether or not to clear the interrupt status register LP_GPIO_STATUS_DATA of GPIO0 ~ GPIO15.
Bit0 ~ bit15 are corresponding to GPIO0 ~ GPIO15. Bit16 ~ bit31 are invalid.
If the value 1 is written to a bit here, the corresponding bit in LP_GPIO_STATUS_DATA will be cleared.

Recommended operation: use this register to clear LP_GPIO_STATUS_DATA.
(WT)
```