

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Register 36.48. MCPWM_GEN2_FORCE_REG (0x00BC)
```

```plaintext
(reserved)
31 16 15 14 13 12 11 10 9 8 7 6 5 0
0 0 0 0 0 0 0 0 0 0 0 0 O 0x20 Reset

MCPWM_GEN2_CNTUFORCE_UPMETHOD Configures updating method for continuous software force of PWM generator 2. When all bits are set to 0: Immediately.
When bitO is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: TEA
When bit3 is set to 1: TEB
When bit4 is set to 1: Sync
When bit5 is set to 1: Disable update
TEA/B here and below means an event generated when the timer's value equals to that of register A/B.
(R/W)

MCPWM_GEN2_A_CNTUFORCE_MODE Configures continuous software force mode for PWM2A.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GEN2_B_CNTUFORCE_MODE Configures continuous software force mode for PWM2B.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GEN2_A_NCIFORCE Configures whether or not to trigger a non-continuous immediate software-force event for PWM2A.
0: No effect
1: Trigger a force event
(R/W)
```

```markdown
Continued on the next page...
```