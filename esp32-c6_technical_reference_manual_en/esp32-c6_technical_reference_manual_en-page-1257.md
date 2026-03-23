

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Register 36.34. MCPWM_GEN1_FORCE_REG (0x0084)
```

```plaintext
(reserved)
31 16 15 14 13 12 11 10 9 8 7 6 5 0
0 0 0 0 0 0 0 0 0 0 0 0 0x20 Reset

MCPWM_GEN1_CNTUFORCE_UPMETHOD Configures updating method for continuous software force of PWM generator 1.
When all bits are set to 0: immediately
When bitO is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: TEA
When bit3 is set to 1: TEB
When bit4 is set to 1: sync
When bit5 is set to 1: disable update
TEA/B here and below means an event generated when the timer’s value equals to that of register A/B.
(R/W)

MCPWM_GEN1_A_CNTUFORCE_MODE Continuous software force mode for PWM1A.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GEN1_B_CNTUFORCE_MODE Configures continuous software force mode for PWM1B.
See details in MCPWM_GEN1_A_CNTUFORCE_MODE. (R/W)

MCPWM_GEN1_A_NCIFORCE Configures whether or not to trigger a non-continuous immediate software-force event for PWM1A
0: No effect
1: Trigger a force event
(R/W)

MCPWM_GEN1_A_NCIFORCE_MODE Configures non-continuous immediate software force mode for PWM1A.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)
```

```markdown
Continued on the next page...
Espressif Systems
1257 ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```