

```markdown
Register 36.51. MCPWM_DT2_CFG_REG (0x00C8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     |    |    |    |    |    |    |    |    |    |    | MCPWM_DT2_CLK_SEL | MCPWM_DT2_A_OUTBYPASS | MCPWM_DT2_B_OUTBYPASS | MCPWM_DT2_FED_INVERTSEL | MCPWM_DT2_FED_OUTINVERT | MCPWM_DT2_RED_OUTINVERT | MCPWM_DT2_RED_INSEL_B_OUTSWAP | MCPWM_DT2_FED_OUTINVERT | MCPWM_DT2_FED_A_OUTSWAP | MCPWM_DT2_RED_UPMETHOD | MCPWM_DT2_FED_UPMETHOD |
|     |    |    |    |    |    |    |    |    |    |    | (reserved) |                |                          |                               |                              |                             |                           |                         |                       |                   |

MCPWM_DT2_FED_UPMETHOD Configures update method for FED (falling edge delay) active register.
O: Immediate.
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_DT2_RED_UPMETHOD Configures update method for RED (rising edge delay) active register. See details in MCPWM_DT2_FED_UPMETHOD. (R/W)

MCPWM_DT2_DEB_MODE S8 in table 36.3-5, dual-edge B mode.
O: fed/red take effect on different path separately
1: fed/red take effect on B path, A out is in bypass or dulpB mode (R/W)

MCPWM_DT2_A_OUTSWAP S6 in table 36.3-5. (R/W)
MCPWM_DT2_B_OUTSWAP S7 in table 36.3-5. (R/W)
MCPWM_DT2_RED_INSEL S4 in table 36.3-5. (R/W)
MCPWM_DT2_FED_INSEL S5 in table 36.3-5. (R/W)
MCPWM_DT2_RED_OUTINVERT S2 in table 36.3-5. (R/W)
MCPWM_DT2_FED_OUTINVERT S3 in table 36.3-5. (R/W)
MCPWM_DT2_A_OUTBYPASS S1 in table 36.3-5. (R/W)
MCPWM_DT2_B_OUTBYPASS S0 in table 36.3-5. (R/W)

MCPWM_DT2_CLK_SEL Configures dead time generator 2 clock selection.
O: PWM_CLK
1: PT_CLK
(R/W)
```