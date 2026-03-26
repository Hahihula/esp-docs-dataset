

```markdown
Register 56.23. MCPWM_CAP_TIMER_CFG_REG (0x00E8)

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | MCPWM_CAP_SYNC_SW | MCPWM_CAP_SYNCLI_SEL | MCPWM_CAP_SYNCLI_EN | MCPWM_CAP_TIMER_EN |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

MCPWM_CAP_TIMER_EN Configures whether to enable capture timer incrementing under APB_CLK.
- 0: Disable
- 1: Enable
(R/W)

MCPWM_CAP_SYNCLI_EN Configures whether to enable capture timer sync.
- 0: Disable
- 1: Enable
(R/W)

MCPWM_CAP_SYNCLI_SEL Configures the selection of capture module sync input.
- 0: None
- 1: Timer0 sync_out
- 2: Timer1 sync_out
- 3: Timer2 sync_out
- 4: SYNC0 from GPIO matrix
- 5: SYNC1 from GPIO matrix
- 6: SYNC2 from GPIO matrix
- 7: None
(R/W)

MCPWM_CAP_SYNC_SW When MCPWM_CAP_SYNCLI_EN is set to 1, configures whether to trigger a capture timer sync so that capture timer is loaded with value in phase register.
- 0: No effect
- 1: Trigger a capture timer sync
(WT)
```