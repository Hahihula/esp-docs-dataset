

```markdown
Register 36.19. MCPWM_GEN0_CFG0_REG (0x0048)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | MCPWM_GEN0_UPMETHOD          |
| 29  | MCPWM_GEN0_TO_SEL            |
| 28  | MCPWM_GEN0_T1_SEL            |
|     |                              |
| 7   | O                           |
| 6   | O                           |
| 5   | O                           |
| 4   | O                           |
| 3   | O                           |
| 2   | O                           |
| 1   | O                           |
| 0   | Reset                       |

MCPWM_GEN0_CFG_UPMETHOD Configures update method for PWM generator 0's active register.
When all bits are set to 0: Immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_GEN0_TO_SEL Configures source selection for PWM generator 0 event_t0, take effect immediately.
0: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: None
(R/W)

MCPWM_GEN0_T1_SEL Configures source selection for PWM generator 0 event_t1, take effect immediately
0: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: None
(R/W)
```