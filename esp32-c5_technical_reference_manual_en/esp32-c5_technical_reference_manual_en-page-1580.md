

```markdown
Register 41.15. MCPWM_DTn_CFG_REG(n: 0-2) (0x0058+0x38*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

MCPWM_DBn_FED_UPMETHOD Configures the update method for FED (Falling edge delay) active register.
O: Immediate
BitO is set to 1: TEZ
Bit1 is set to 1: TEP
Bit2 is set to 1: Sync
Bit3 is set to 1: Disable the update
(R/W)

MCPWM_DBn_RED_UPMETHOD Configures the update method for RED (Rising edge delay) active register.
O: Immediate
BitO is set to 1: TEZ
Bit1 is set to 1: TEP
Bit2 is set to 1: Sync
Bit3 is set to 1: Disable the update
(R/W)

MCPWM_DBn_DEB_MODE Configures the S8 switch in Table 41.3-5.
O: FED/RED take effect on different paths separately
1: FED/RED take effect on B path, A out is in bypass or dulpB mode
(R/W)

MCPWM_DBn_A_OUTSWAP Configures the S6 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_B_OUTSWAP Configures the S7 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_RED_INSEL Configures the S4 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_FED_INSEL Configures the S5 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)

MCPWM_DBn_RED_OUTINVERT Configures the S2 switch in Table 41.3-5. For typical configurations, please refer to Table 41.3-6. (R/W)
```
Continued on the next page...
```