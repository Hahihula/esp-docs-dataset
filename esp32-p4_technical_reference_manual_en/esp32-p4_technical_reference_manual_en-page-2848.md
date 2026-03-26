

```markdown
Chapter 56 Motor Control PWM (MCPWM)

Register 56.12. MCPWM_GENn_FORCE_REG(n: 0-2) (0x004C+0x38*n)
```

```text
(reserved)
MCPWM_GEN_B_NCIFORCE_MODE
MCPWM_GEN_A_NCIFORCE_MODE
MCPWM_GEN_B_CNTUFORCE_MODE
MCPWM_GEN_A_CNTUFORCE_MODE
MCPWM_GEN_B_CNTUFORCE_UPMETHOD
MCPWM_GEN_A_CNTUFORCE_UPMETHOD

31 16 15 14 13 12 11 10 9 8 7 6 5 0
+----+----+----+----+----+----+----+----+----+----+----+
|    |    |    |    |    |    |    |    |    |    | Reset |
+----+----+----+----+----+----+----+----+----+----+----+
| 0x20 |    |    |    |    |    |    |    |    |    |    |
+----+----+----+----+----+----+----+----+----+----+----+

MCPWM_GENn_CNTUFORCE_UPMETHOD Configures the update method for continuous software force of PWM generator n.
When all bits are set to 0: Immediately
When bitO is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: TEA
When bit3 is set to 1: TEB
When bit4 is set to 1: Sync
When bit5 is set to 1: Disable update
TEA/B means an event generated when the timer's value equals to that of register A/B.
(R/W)

MCPWM_GENn_A_CNTUFORCE_MODE Configures the continuous software force mode for PWM n
A.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GENn_B_CNTUFORCE_MODE Configures the continuous software force mode for PWM n
B.
0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GENn_A_NCIFORCE Configures whether to trigger the non-continuous immediate software-force event for PWM n A.
0: Invalid
1: Trigger a force event
(R/W)

Continued on the next page...
```

```markdown
Espressif Systems    2848    ESP32-P4 TRM
Submit Documentation Feedback PRELIMINARY
```