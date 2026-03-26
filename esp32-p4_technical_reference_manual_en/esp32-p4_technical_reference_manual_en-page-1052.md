

```markdown
|31|30|23|22|15|14|13|12|11|9|8|7|6|0|
|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
||0x80||0x40||0|0|0| |1|0|0|0| |
||||||||Reset||
```

**PMU_OP2A_FORCE_TIEH_SEL_O** Configures which of the following controls the mode selection for VO3 regulator.

- O: Mode selection is controlled by `PMU_OP2A_TIEH_SEL_O`
- 1: Mode selection is controlled by SDMMC_0
- 2: Bypass mode
- 3: Mode selection is controlled by SDMMC_1

(R/W)

**PMU_OP2A_XPD_O** Configures whether software enables VO3 regulator.

- O: Disable
- 1: Enable

(R/W)

**PMU_OP2A_TIEH_SEL_O** Configures mode for VO3.

- O: Mode is controlled by `PMU_OP2A_TIEH_O`.
- 1: Mode is controlled by SDMMC_0
- 2: Bypass mode
- 3: Mode is controlled by SDMMC_1

(R/W)

**PMU_OP2A_TIEH_O** Configures mode for VO3.

- O: LDO mode
- 1: Bypass mode

(R/W)

**PMU_OP2A_TARGET1_O** Configures the timeout for stage 2 of the VO3 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)

**PMU_OP2A_TARGETO_O** Configures the timeout for stage 1 of the VO3 regulator wait counter, with the unit being a 16 division of LP_DYN_SLOW_CLK. (R/W)
```