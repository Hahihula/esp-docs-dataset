

```markdown
Register 8.39. GPIO_EXT_INT_ST_REG (0x01D4)

| 31 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|
|    | Reset |

GPIO_EXT_COMP_NEG_O_INT_ST The interrupt status of GPIO_EXT_COMP_NEG_O_INT.
(RO)

GPIO_EXT_COMP_POS_O_INT_ST The interrupt status of GPIO_EXT_COMP_POS_O_INT.
(RO)

GPIO_EXT_COMP_ALL_O_INT_ST The interrupt status of GPIO_EXT_COMP_ALL_O_INT.
(RO)


Register 8.40. GPIO_EXT_INT_ENA_REG (0x01D8)

| 31 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|
|    | Reset |

GPIO_EXT_COMP_NEG_O_INT_ENA Write 1 to enable GPIO_EXT_COMP_NEG_O_INT.
(R/W)

GPIO_EXT_COMP_POS_O_INT_ENA Write 1 to enable GPIO_EXT_COMP_POS_O_INT.
(R/W)

GPIO_EXT_COMP_ALL_O_INT_ENA Write 1 to enable GPIO_EXT_COMP_ALL_O_INT.
(R/W)
```