

```markdown
Register 7:10. GPIO_STATUS_W1TS_REG (0x0048)

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_STATUS_W1TS Configures whether or not to set the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO30.

- Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid.
- If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be set to 1.
- Recommended operation: use this register to set GPIO_STATUS_INTERRUPT.
(WT)

Register 7:11. GPIO_STATUS_W1TC_REG (0x004C)

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO30.

- Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid.
- If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be cleared.
- Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.
(WT)
```