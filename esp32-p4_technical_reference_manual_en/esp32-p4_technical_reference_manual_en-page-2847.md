

```markdown
Register 56.11. MCPWM_GENn_CFGO_REG(n: 0-2) (0x0048+0x38*n)

| bit 31 | ... | 10 | 9 | 7 | 6 | 4 | 3 | 0 |
|--------|-----|-----|---|---|---|---|---|---|
|        | (reserved) | MCPWM_GENn_T1_SEL | MCPWM_GENn_TO_SEL | MCPWM_GENn_CFGP_UPMETHOD | Reset |

MCPWM_GENn_CFG_UPMETHOD Configures the update method for PWM generator n's active register.
When all bits are set to 0: Immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_GENn_TO_SEL Configures source selection for PWM generator n event_t0, take effect immediately.
0: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: Invalid, selects nothing (R/W)

MCPWM_GENn_T1_SEL Configures source selection for PWM generator n event_t1, take effect immediately.
0: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: Invalid, selects nothing (R/W)
```