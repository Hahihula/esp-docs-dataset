

```markdown
Register 56.5. MCPWM_TIMERn_STATUS_REG(n: 0-2) (0x0010+0x10*n)

| Bit 31 | ... | 17 | 16 | 15 |
|--------|-----|----|----|----|
|        |     |    |    | MCPWM_TIMERn_DIRECTION |
|        |     |    |    | (reserved) |
|        |     |    |    | MCPWM_TIMERn_VALUE |

MCPWM_TIMERn_VALUE Represents current PWM timer n counter value. (RO)

MCPWM_TIMERn_DIRECTION Represents current PWM timer n counter direction.
0: Increment
1: Decrement
(RO)
```

```markdown
Register 56.6. MCPWM_TIMER_SYNCI_CFG_REG (0x0034)

| Bit 31 | ... | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|----|----|----|---|---|---|---|---|---|---|---|---|---|
|        |     |    |    |    |   |   | MCPWM_TIMERn_SYNCI_SEL | MCPWM_TIMERn_SYNCI_INVERT | (reserved) |

MCPWM_TIMERn_SYNCI_SEL Configures sync input for PWM timer n.
1: PWM timer0 sync out
2: PWM timer1 sync out
3: PWM timer2 sync out
4: SYNC0 from GPIO matrix
5: SYNC1 from GPIO matrix
6: SYNC2 from GPIO matrix
Other values: no sync input selected (R/W)

MCPWM_EXTERNAL_SYNCI_INVERT Configures whether to invert SYNCn from GPIO matrix.
0: Not invert
1: Invert
(R/W)
```