

```markdown
Register 36.37. MCPWM_DT1_CFG_REG (0x0090)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    |    |    |    |    |    |    |    | Reset |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) |
```

MCPWM_DT1_FED_UPMETHOD Configures update method for FED (falling edge delays) active register.
0: immediate.
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_DT1_RED_UPMETHOD Configures update method for RED (rising edge delay) active register. See details in MCPWM_DT1_FED_UPMETHOD. (R/W)

MCPWM_DT1_DEB_MODE Configures the S8 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_A_OUTSWAP Configures the S6 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_B_OUTSWAP Configures the S7 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_RED_INSEL Configures the S4 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_FED_INSEL Configures the S5 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_RED_OUTINVERT Configures the S2 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_FED_OUTINVERT Configures the S3 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_A_OUTBYPASS Configures the S1 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_B_OUTBYPASS Configures the SO switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT1_CLK_SEL Configures the dead time generator 1 clock selection.
0: PWM_CLK.
1: PT_CLK.
(R/W)
```