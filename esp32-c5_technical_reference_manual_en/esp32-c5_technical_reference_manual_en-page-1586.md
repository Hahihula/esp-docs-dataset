

```markdown
Register 41.20. MCPWM_FHn_CFG1_REG(n: 0-2) (0x006C+0x38*n)
```

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 5  | 4  | 3  | 2  | 1  |
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |

MCPWM_TZn_CLR_OST Configures whether to generate a one-shot mode action clear by software.
- O: No effect
- 1: Triggers a clear for ongoing one-shot mode action by software (R/W)

MCPWM_TZn_CBCPULSE Configures the refresh moment selection of cycle-by-cycle mode action.
- O: Select nothing, will not refresh
- Bit0 is set to 1: TEZ
- Bit1 is set to 1: TEP (R/W)

MCPWM_TZn_FORCE_CBC Configures whether to generate a software cycle-by-cycle mode action.
- O: No effect
- 1: Triggers a cycle-by-cycle mode action by software (R/W)

MCPWM_TZn_FORCE_OST Configures whether to generate a software one-shot mode action.
- O: No effect
- 1: Triggers a one-shot mode action by software (R/W)
```