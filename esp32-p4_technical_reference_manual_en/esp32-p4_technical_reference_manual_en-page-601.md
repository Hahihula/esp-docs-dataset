

```markdown
## Register 9.41. GPIO_INT_ENA_REG (0x0708)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 6   | GPIO_COMPO_ALL_INT_ENA                                                     |
| 5   | GPIO_COMPL_POS_INT_ENA                                                     |
| 4   | GPIO_COMPL_NEG_INT_ENA                                                     |
| 3   | GPIO_COMPO_POS_INT_ENA                                                     |
| 2   | GPIO_COMPO_NEG_INT_ENA                                                     |
| 1   | Reset                                                                      |

- GPIO_COMPO_NEG_INT_ENA Write 1 to enable GPIO_COMPO_NEG_INT. (R/W)
- GPIO_COMPO_POS_INT_ENA Write 1 to enable GPIO_COMPO_POS_INT. (R/W)
- GPIO_COMPO_ALL_INT_ENA Write 1 to enable GPIO_COMPO_ALL_INT. (R/W)
- GPIO_COMPL_NEG_INT_ENA Write 1 to enable GPIO_COMPL_NEG_INT. (R/W)
- GPIO_COMPL_POS_INT_ENA Write 1 to enable GPIO_COMPL_POS_INT. (R/W)
- GPIO_COMPL_ALL_INT_ENA Write 1 to enable GPIO_COMPL_ALL_INT. (R/W)

## Register 9.42. GPIO_INT_CLR_REG (0x070C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 6   | GPIO_COMPL_ALL_INT_CLR                                                     |
| 5   | GPIO_COMPL_POS_INT_CLR                                                     |
| 4   | GPIO_COMPL_NEG_INT_CLR                                                     |
| 3   | GPIO_COMPO_POS_INT_CLR                                                     |
| 2   | GPIO_COMPO_NEG_INT_CLR                                                     |
| 1   | Reset                                                                      |

- GPIO_COMPO_NEG_INT_CLR Write 1 to clear GPIO_COMPO_NEG_INT. (WT)
- GPIO_COMPO_POS_INT_CLR Write 1 to clear GPIO_COMPO_POS_INT. (WT)
- GPIO_COMPO_ALL_INT_CLR Write 1 to clear GPIO_COMPO_ALL_INT. (WT)
- GPIO_COMPL_NEG_INT_CLR Write 1 to clear GPIO_COMPL_NEG_INT. (WT)
- GPIO_COMPL_POS_INT_CLR Write 1 to clear GPIO_COMPL_POS_INT. (WT)
- GPIO_COMPL_ALL_INT_CLR Write 1 to clear GPIO_COMPL_ALL_INT. (WT)

## 9.20.2 HP IO MUX Registers

The addresses in this section are relative to the HP IO MUX base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX.
```