

```markdown
Register 7.6. GPIO_ENABLE_W1TC_REG (0x0028)

| Bit | Field         | Description                                                                 |
|-----|---------------|-----------------------------------------------------------------------------|
| 31  |              | 0                                                                             |
|     |               | Reset                                                                         |
|     |               | 0x000000                                                                      |

GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register GPIO_ENABLE_REG of GPIO0 ~ GPIO30.
- 0: Not clear
- 1: The corresponding bit in GPIO_ENABLE_REG will be cleared
  Bit0 ~ bit30 are corresponding to GPIO0 ~ 30. Bit31 is invalid. Recommended operation: use this register to clear GPIO_ENABLE_REG.

(WT)

Register 7.7. GPIO_STRAP_REG (0x0038)

| Bit | Field         | Description                                                                 |
|-----|---------------|-----------------------------------------------------------------------------|
| 31  |              | 0                                                                             |
|     |               | Reset                                                                         |
|     |               | 0x00                                                                          |

GPIO_STRAPPING Represents the values of GPIO strapping pins.
- bit0 ~ bit1: invalid
- bit2: GPIO8
- bit3: GPIO9
- bit4: GPIO15
- bit5: MTMS
- bit6: MTDI
- bit7 ~ bit15: invalid

(RO)
```