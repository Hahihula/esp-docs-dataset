

```markdown
Register 36.46. MCPWM_GEN2_TSTMP_B_REG (0x00B4)

MCPWM_GEN2_B Shadow register for PWM generator 2 time stamp B. (R/W)


Register 36.47. MCPWM_GEN2_CFG0_REG (0x00B8)

MCPWM_GEN2_CFG_UPMETHOD Configures update method for PWM generator 2’s active register.
O: Immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: sync
When bit3 is set to 1: disable the update
(R/W)

MCPWM_GEN2_TO_SEL Source selection for PWM generator 2 event_t0, take effect immediately.
O: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: None
(R/W)

MCPWM_GEN2_T1_SEL Source selection for PWM generator 2 event_t1, take effect immediately.
O: fault_event0
1: fault_event1
2: fault_event2
3: sync_taken
4: None
(R/W)
```