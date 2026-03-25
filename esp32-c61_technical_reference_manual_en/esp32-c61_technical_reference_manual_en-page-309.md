

```markdown
Chapter 6 GPIO Matrix and IO MUX

Register 6.35. GPIO_EXT_INT_RAW_REG (0x01D0)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 3   | 2                                   | 1                                                                               |
|     | Reset                               | 0                                                                               |

GPIO_EXT_COMP_NEG_O_INT_RAW The raw interrupt status of GPIO_EXT_COMP_NEG_O_INT.
(RO/WTC/SS)

GPIO_EXT_COMP_POS_O_INT_RAW The raw interrupt status of GPIO_EXT_COMP_POS_O_INT.
(RO/WTC/SS)

GPIO_EXT_COMP_ALL_O_INT_RAW The raw interrupt status of GPIO_EXT_COMP_ALL_O_INT.
(RO/WTC/SS)

Register 6.36. GPIO_EXT_INT_ST_REG (0x01D4)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 3   | 2                                   | 1                                                                               |
|     | Reset                               | 0                                                                               |

GPIO_EXT_COMP_NEG_O_INT_ST The interrupt status of GPIO_EXT_COMP_NEG_O_INT.
(RO)

GPIO_EXT_COMP_POS_O_INT_ST The interrupt status of GPIO_EXT_COMP_POS_O_INT.
(RO)

GPIO_EXT_COMP_ALL_O_INT_ST The interrupt status of GPIO_EXT_COMP_ALL_O_INT.
(RO)
```