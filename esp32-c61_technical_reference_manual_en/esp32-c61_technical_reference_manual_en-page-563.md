

```markdown
Register 11.55. PMU_IMM_PAD_HOLD_ALL_REG (0x00E4)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                             | (reserved)                                                                   |
| 30  | PMU_TIE_LOW_HP_PAD_HOLD_ALL          | Configures whether to force the PMU LP GPIO HOLD signal to high.            |
|     |                                      | O: No effect                                                                 |
|     |                                      | 1: Force to high                                                             |
|     | (WT)                                 |                                                                             |
| 29  | PMU_TIE_LOW_LP_PAD_HOLD_ALL          | Configures whether to force the PMU LP GPIO HOLD signal to low.             |
|     |                                      | O: No effect                                                                 |
|     |                                      | 1: Force to low                                                              |
|     | (WT)                                 |                                                                             |
| 28  | PMU_TIE_HIGH_HP_PAD_HOLD_ALL         | Configures whether to force the PMU HP GPIO HOLD signal to high.            |
|     |                                      | O: No effect                                                                 |
|     |                                      | 1: Force to high                                                             |
|     | (WT)                                 |                                                                             |
| 27  | PMU_TIE_LOW_HP_PAD_HOLD_ALL          | Configures whether to force the PMU HP GPIO HOLD signal to low.             |
|     |                                      | O: No effect                                                                 |
|     |                                      | 1: Force to low                                                              |
|     | (WT)                                 |                                                                             |

PMU_TIE_HIGH_LP_PAD_HOLD_ALL   Configures whether to force the PMU LP GPIO HOLD signal to high.
O: No effect
1: Force to high
(WT)

PMU_TIE_LOW_LP_PAD_HOLD_ALL    Configures whether to force the PMU LP GPIO HOLD signal to low.
O: No effect
1: Force to low
(WT)

PMU_TIE_HIGH_HP_PAD_HOLD_ALL   Configures whether to force the PMU HP GPIO HOLD signal to high.
O: No effect
1: Force to high
(WT)

PMU_TIE_LOW_HP_PAD_HOLD_ALL    Configures whether to force the PMU HP GPIO HOLD signal to low.
O: No effect
1: Force to low
(WT)
```