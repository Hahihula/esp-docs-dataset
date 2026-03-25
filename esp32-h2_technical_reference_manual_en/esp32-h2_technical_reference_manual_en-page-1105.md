

```markdown
Chapter 36 Motor Control PWM (MCPWM)                                     GoBack


Register 36.13. MCPWM_TIMER2_STATUS_REG (0x0030)

[Diagram: Register bit field layout]

31 ────────────────┬───────────────┬───────────────┬───────────────┐
                   │ reserved      │ MCPWM_TIMER2_DIRECTION │ MCPWM_TIMER2_VALUE │
                   │               │                 │                │
                   └───────────────┴───────────────┴───────────────┘
                    0

MCPWM_TIMER2_VALUE   Represents current PWM timer2 counter value. (RO)

MCPWM_TIMER2_DIRECTION  Represents current PWM timer2 counter direction.
    0: Increment
    1: Decrement
    (RO)
```