

```markdown
Register 6.37. GPIO_EXT_INT_ENA_REG (0x01D8)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 3   | 2                                   | 1                                                                               | Reset
|     | GPIO_EXT_COMP_NEG_O_INT_ENA         | Write 1 to enable GPIO_EXT_COMP_NEG_O_INT. (R/W)                           |
|     | GPIO_EXT_COMP_POS_O_INT_ENA         | Write 1 to enable GPIO_EXT_COMP_POS_O_INT. (R/W)                           |
|     | GPIO_EXT_COMP_ALL_O_INT_ENA         | Write 1 to enable GPIO_EXT_COMP_ALL_O_INT. (R/W)                           |

Register 6.38. GPIO_EXT_INT_CLR_REG (0x01DC)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 3   | 2                                   | 1                                                                               | Reset
|     | GPIO_EXT_COMP_NEG_O_INT_CLR         | Write 1 to clear GPIO_EXT_COMP_NEG_O_INT. (WT)                             |
|     | GPIO_EXT_COMP_POS_O_INT_CLR         | Write 1 to clear GPIO_EXT_COMP_POS_O_INT. (WT)                             |
|     | GPIO_EXT_COMP_ALL_O_INT_CLR         | Write 1 to clear GPIO_EXT_COMP_ALL_O_INT. (WT)                             |
```