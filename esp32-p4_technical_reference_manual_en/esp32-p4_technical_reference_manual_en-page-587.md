

```markdown
Register 9.17. GPIO_STATUS_W1TS_REG (0x0048)

GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO31.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31.
If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be set to 1.

Recommended operation: use this register to set GPIO_STATUS_INTERRUPT.
(WT)

Register 9.18. GPIO_STATUS_W1TC_REG (0x004C)

GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO31.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31.
If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be cleared.

Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.
(WT)
```