

```markdown
Register 36.32. MCPWM_GEN1_TSTMP_B_REG (0x007C)

MCPWM_GEN1_B Shadow register for PWM generator 1 time stamp B. (R/W)


Register 36.33. MCPWM_GEN1_CFG0_REG (0x0080)

MCPWM_GEN1_CFG_UPMETHOD Configures update method for PWM generator 1's active register of configuration.
When all bits are set to 0: immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: sync
When bit3 is set to 1: disable the update
(R/W)

MCPWM_GEN1_TO_SEL Configures source selection for PWM generator 1 event_tO, take effect immediately.
0: fault_event0
1: fault_event1.
2: fault_event2
3: sync_taken
4: None
(R/W)

MCPWM_GEN1_T1_SEL Configures source selection for PWM generator 1 event_t1, take effect immediately. See details in MCPWM_GEN1_TO_SEL. (R/W)
```