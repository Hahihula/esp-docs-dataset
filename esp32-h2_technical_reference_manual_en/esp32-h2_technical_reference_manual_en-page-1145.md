

```markdown
Register 36.55. MCPWM_FH2_CFG0_REG (0x00D8)
```

Continued from the previous page...

MCPWM_FH2_FO_OST Configures whether or not fault_eventO will trigger one-shot mode action.
- O: No effect
- 1: Trigger
(R/W) (R/W)

MCPWM_FH2_A_CBC_D Configures cycle-by-cycle mode action on PWM2A when fault event occurs and timer is decreasing.
- O: Do nothing.
- 1: Force low.
- 2: Force high.
- 3: Toggle
(R/W)

MCPWM_FH2_A_CBC_U Configures cycle-by-cycle mode action on PWM2A when fault event occurs and the timer is increasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_A_OST_D Configures one-shot mode action on PWM2A when fault event occurs and timer is decreasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_A_OST_U Configures one-shot mode action on PWM2A when fault event occurs and timer is increasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_B_CBC_D Configures cycle-by-cycle mode action on PWM2B when fault event occurs and timer is decreasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_B_CBC_U Configures cycle-by-cycle mode action on PWM2B when fault event occurs and timer is increasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_B_OST_D Configures one-shot mode action on PWM2B when fault event occurs and timer is decreasing. See details in MCPWM_FH2_A_CBC_D. (R/W)

MCPWM_FH2_B_OST_U Configures one-shot mode action on PWM2B when fault event occurs and timer is increasing. See details in MCPWM_FH2_A_CBC_D. (R/W)
```