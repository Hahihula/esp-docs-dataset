

```markdown
Register 62.1. ADC_CTRL_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 18 | 17 | 15 | 14 | 13 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|
|     |    | (reserved) | ADC_XPD_SAR2_FORCE | ADC_XPD_SAR1_FORCE | (reserved) | ADC_SAR2_PATT_P_CLEAR | ADC_SAR1_PATT_P_CLEAR | ADC_SAR2_PATT_LEN | ADC_SAR1_PATT_LEN | ADC_SAR_CLK_DIV | ADC_SAR_CLK_GATED | ADC_SAR_SEL | ADC_WORK_MODE | reserved |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 15 | 15 | 4 | 1 | 0 | 0 | Reset |

ADC_WORK_MODE Configures dual HP ADC sampling.
O: Single HP ADC sampling
1: Dual HP ADC simultaneous sampling
2: Dual HP ADC alternative sampling.
(R/W)

ADC_SAR_SEL Configures which HP ADC to use for single HP ADC sampling.
O: Use HP ADC1
1: Use HP ADC2
(R/W)

ADC_SAR_CLK_GATED Enable HP ADC clock gate when HP ADC is in idle.
O: Disable
1: Enable
(R/W)

ADC_SAR_CLK_DIV Configures HP ADC clock division. Division = configured value + 1. (R/W)

ADC_SAR1_PATT_LEN Configures how many pattern table entries will be used for HP ADC1.
O: Use only cmd0
1: Use cmd0 and cmd1
n: Use cmd0 to cmdn, the maximum n is 7
(R/W)

ADC_SAR2_PATT_LEN Configures how many pattern table entries will be used for HP ADC2.
O: Use only cmd0
1: Use cmd0 and cmd1
n: Use cmd0 to cmdn, the maximum n is 7
(R/W)

ADC_SAR1_PATT_P_CLEAR Clears the pointer of pattern table for HP ADC1 Controller.
O: No effect
1: Clear
(R/W)

ADC_SAR2_PATT_P_CLEAR Clears the pointer of pattern table for HP ADC2 Controller.
O: No effect
1: Clear
(R/W)
```