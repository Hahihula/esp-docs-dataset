

```markdown
|31|30|23|22|15|14|13|12|11|9|8|7|6|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
||0x80||0x40||0| | | ||||||Reset|

PMU_OP1A_FORCE_TIEH_SEL_1 Configures which of the following controls the mode selection for VO2 regulator.
0: Mode selection is controlled by PMU_OP1A_TIEH_SEL_1
1: Mode selection is controlled by SDMMC_O
2: Bypass mode
3: Mode selection is controlled by SDMMC_1
(R/W)

PMU_OP1A_XPD_1 Configures whether software enables VO2 regulator.
0: Disable
1: Enable
(R/W)

PMU_OP1A_TIEH_SEL_1 Configures mode for VO2.
0: Mode is controlled by PMU_OP1A_TIEH_1.
1: Mode is controlled by SDMMC_O
2: Bypass mode
3: Mode is controlled by SDMMC_1
(R/W)

PMU_OP1A_TIEH_1 Configures mode for VO2.
0: LDO mode
1: Bypass mode
(R/W)

PMU_OP1A_TARGET1_1 Configures the timeout for stage 2 of the VO2 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)

PMU_OP1A_TARGET0_1 Configures the timeout for stage 1 of the VO2 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)
```