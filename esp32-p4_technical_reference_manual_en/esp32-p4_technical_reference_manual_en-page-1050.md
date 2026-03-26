

```markdown
## Register 14.57. PMU_HP_LP_CPU_COMM_REG (0x019C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                    |
| 30  | PMU_LP_TRIGGER_HP                                                           |
| 29  | PMU_HP_TRIGGER_LP                                                          |

PMU_LP_TRIGGER_HP When the LP CPU sets this register to 1, the chip is woken up. (WT)
PMU_HP_TRIGGER_LP When the HP CPU sets this register to 1, the LP CPU is woken up. (WT)

## Register 14.58. PMU_EXT_LDO_PO_OP1A_REG (0x01B8)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                    |
| 30  | PMU_OP1A_TARGETO_O                                                          |
| 29  | PMU_OP1A_TARGET1_O                                                         |
| 28  | PMU_OP1A_TIEH_SEL_O                                                        |
| 27  | PMU_OP1A_TIEH_O                                                            |
| 26  | reserved                                                                   |
| 25  | PMU_OP1A_TIEH_SEL_O                                                        |
| 24  | PMU_OP1A_TIEH_O                                                            |
| 23  | reserved                                                                   |
| 22  | PMU_OP1A_TIEH_SEL_O                                                        |
| 21  | PMU_OP1A_TIEH_O                                                            |
| 20  | reserved                                                                   |
| 19  | PMU_OP1A_TIEH_SEL_O                                                        |
| 18  | PMU_OP1A_TIEH_O                                                            |
| 17  | reserved                                                                   |
| 16  | PMU_OP1A_TIEH_SEL_O                                                        |
| 15  | PMU_OP1A_TIEH_O                                                            |
| 14  | reserved                                                                   |
| 13  | PMU_OP1A_TIEH_SEL_O                                                        |
| 12  | PMU_OP1A_TIEH_O                                                            |
| 11  | reserved                                                                   |
| 10  | PMU_OP1A_TIEH_SEL_O                                                        |
| 9   | PMU_OP1A_TIEH_O                                                            |
| 8   | reserved                                                                   |
| 7   | PMU_OP1A_TIEH_SEL_O                                                        |
| 6   | PMU_OP1A_TIEH_O                                                            |

PMU_OP1A_FORCE_TIEH_SEL_O Configures which of the following controls the mode selection for VO1 regulator.
1: Mode selection is controlled by PMU_OP1A_TIEH_SEL_O
0: Mode selection is controlled by eFuse (R/W)

PMU_OP1A_TIEH_SEL_O Configures mode for VO1.
0: Mode is controlled by PMU_OP1A_TIEH_O.
1: Mode is controlled by SDMMC_O
2: Bypass mode
3: Mode is controlled by SDMMC_1 (R/W)

PMU_OP1A_TIEH_O Configures mode for VO1.
0: LDO mode
1: Bypass mode (R/W)

PMU_OP1A_TARGET1_O Configures the timeout for stage 2 of the VO1 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)

PMU_OP1A_TARGETO_O Configures the timeout for stage 1 of the VO1 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)
```