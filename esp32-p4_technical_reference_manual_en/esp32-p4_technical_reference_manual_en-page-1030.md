

```markdown
Register 14.32. PMU_IMM_PAD_HOLD_ALL_REG (0x00E4)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                |                                                                             |
| 30  |                                |                                                                             |
| 29  |                                |                                                                             |
| 28  |                                |                                                                             |
| 27  |                                |                                                                             |
| 26  |                                |                                                                             |
| 25  |                                |                                                                             |
|     | PMU_PAD_SLP_SEL               | Indicates whether the current GPIO function uses sleep configurations.      |
|     | O: No                         |                                                                                   |
|     | 1: Yes                        |                                                                                   |
|     | (RO)                          |                                                                                   |
|     | PMU_LP_PAD_HOLD_ALL           | Indicates whether the LP PAD is in the HOLD status.                           |
|     | O: No                         |                                                                                   |
|     | 1: Yes                        |                                                                                   |
|     | (RO)                          |                                                                                   |
|     | PMU_HP_PAD_HOLD_ALL           | Represents whether the HP PAD is in the HOLD status.                          |
|     | O: No                         |                                                                                   |
|     | 1: Yes                        |                                                                                   |
|     | (RO)                          |                                                                                   |
|     | PMU_TIE_LOW_HP_PAD_HOLD_ALL   | Immediately configures GPIO function to use sleep configurations.            |
|     | (WT)                          |                                                                                   |
|     | PMU_TIE_LOW_PAD_SLP_SEL       | Immediately releases GPIO function from using sleep configuration.           |
|     | (WT)                          |                                                                                   |
|     | PMU_TIE_HIGH_LP_PAD_HOLD_ALL  | Immediately configure LP PAD to enter HOLD state. (WT)                        |
|     | PMU_TIE_LOW_LP_PAD_HOLD_ALL   | Immediately releases LP PAD from HOLD state. (WT)                             |
|     | PMU_TIE_HIGH_HP_PAD_HOLD_ALL  | Immediately configures HP PAD to enter HOLD state. (WT)                       |
|     | PMU_TIE_LOW_HP_PAD_HOLD_ALL   | Immediately releases HP PAD from HOLD state. (WT)                             |

PMU_PAD_SLP_SEL Indicates whether the current GPIO function uses sleep configurations.
O: No
1: Yes
(RO)

PMU_LP_PAD_HOLD_ALL Indicates whether the LP PAD is in the HOLD status.
O: No
1: Yes
(RO)

PMU_HP_PAD_HOLD_ALL Represents whether the HP PAD is in the HOLD status.
O: No
1: Yes
(RO)

PMU_TIE_LOW_HP_PAD_HOLD_ALL Immediately configures GPIO function to use sleep configurations. (WT)
PMU_TIE_LOW_PAD_SLP_SEL Immediately releases GPIO function from using sleep configuration. (WT)
PMU_TIE_HIGH_LP_PAD_HOLD_ALL Immediately configure LP PAD to enter HOLD state. (WT)
PMU_TIE_LOW_LP_PAD_HOLD_ALL Immediately releases LP PAD from HOLD state. (WT)
PMU_TIE_HIGH_HP_PAD_HOLD_ALL Immediately configures HP PAD to enter HOLD state. (WT)
PMU_TIE_LOW_HP_PAD_HOLD_ALL Immediately releases HP PAD from HOLD state. (WT)

(reserved)
```
```markdown
| 31 | 30 | 29 | 28 | 27 | 26 | 25 | ... | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|-----|---|---|---|---|
| 0  | 0  | 0  | 0  | 0  | 0  | 0  | ... | 0 | 0 | 0 | Reset |
```