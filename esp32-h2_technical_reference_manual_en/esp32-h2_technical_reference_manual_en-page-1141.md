

```markdown
Register 36.51. MCPWM_DT2_CFG_REG (0x00C8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    |    |    |    |    |    |    |    |    | MCPWM_DT2_CLK_SEL | MCPWM_DT2_A_OUTBYPASS | MCPWM_DT2_B_OUTBYPASS | MCPWM_DT2_RED_INSEL | MCPWM_DT2_FED_INSEL | MCPWM_DT2_RED_OUTINVERT | MCPWM_DT2_FED_OUTINVERT | MCPWM_DT2_A_OUTSWAP | MCPWM_DT2_B_OUTSWAP | MCPWM_DT2_RED_MODE | MCPWM_DT2_FED_UPMETHOD | (reserved) |
```

MCPWM_DT2_FED_UPMETHOD Configures update method for FED (falling edge delay) active register.
O: Immediate.
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_DT2_RED_UPMETHOD Configures update method for RED (rising edge delay) active register. See details in MCPWM_DT2_FED_UPMETHOD. (R/W)

MCPWM_DT2_DEB_MODE Configures the S8 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_A_OUTSWAP Configures the S6 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_B_OUTSWAP Configures the S7 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_RED_INSEL Configures the S4 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_FED_INSEL Configures the S5 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_RED_OUTINVERT Configures the S2 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_FED_OUTINVERT Configures the S3 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_A_OUTBYPASS Configures the S1 switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_B_OUTBYPASS Configures the SO switch in Table 36.3-5. For typical configurations, please refer to Table 36.3-6. (R/W)

MCPWM_DT2_CLK_SEL Configures dead time generator 2 clock selection.
O: PWM_CLK
1: PT_CLK

(R/W)
```