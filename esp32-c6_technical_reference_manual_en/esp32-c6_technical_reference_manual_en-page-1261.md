

```markdown
Register 36.37. MCPWM_DT1_CFG_REG (0x0090)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    |    |    |    |    |    |    |    | Reset |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
```

MCPWM_DT1_FED_UPMETHOD Configures update method for FED (falling edge delays) active register.
0: immediate.
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_DT1_RED_UPMETHOD Configures update method for RED (rising edge delay) active register. See details in MCPWM_DT1_FED_UPMETHOD. (R/W)

MCPWM_DT1_DEB_MODE S8 in table 36.3-5, dual-edge B mode.
0: fed/red take effect on different path separately
1: fed/red take effect on B path, A out is in bypass or dulpB mode (R/W)

MCPWM_DT1_A_OUTSWAP S6 in table 36.3-5. (R/W)

MCPWM_DT1_B_OUTSWAP S7 in table 36.3-5. (R/W)

MCPWM_DT1_RED_INSEL S4 in table 36.3-5. (R/W)

MCPWM_DT1_FED_INSEL S5 in table 36.3-5. (R/W)

MCPWM_DT1_RED_OUTINVERT S2 in table 36.3-5. (R/W)

MCPWM_DT1_FED_OUTINVERT S3 in table 36.3-5. (R/W)

MCPWM_DT1_A_OUTBYPASS S1 in table 36.3-5. (R/W)

MCPWM_DT1_B_OUTBYPASS SO in table 36.3-5. (R/W)

MCPWM_DT1_CLK_SEL Configures the dead time generator 1 clock selection.
0: PWM_CLK.
1: PT_CLK.
(R/W)
```