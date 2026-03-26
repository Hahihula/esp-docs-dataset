

```markdown
Register 9.9. GPIO_ENABLE_W1TC_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |

Reset: 0x000000

GPIO_ENABLE_W1TC Configures whether or not to clear the output enable register GPIO_ENABLE_REG of GPIO0 ~ GPIO31.
- 0: Not clear
- 1: The corresponding bit in GPIO_ENABLE_REG will be cleared
  Bit0 ~ bit31 are corresponding to GPIO00 ~ GPIO31. Recommended operation: use this register to clear GPIO_ENABLE_REG.

(WT)

Register 9.10. GPIO_ENABLE1_REG (0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 25  | 0                                                                             |
| 24  | 0                                                                             |

Reset: 0x000000

GPIO_ENABLE1_DATA Configures whether or not to enable the output of GPIO32 ~ GPIO54.
- 0: Not enable
- 1: Enable
  Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54.
(R/W/WTC)
```