

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Register 36.20. MCPWM_GENO_FORCE_REG (0x004C)
```

![Register Bitfield Diagram](image_description: A bitfield diagram for register 0x004C showing bits 31 down to 0, with specific fields labeled such as "reserved", and various force mode configuration bits like MCPWM_GENO_B_NCIFORCE_MODE, MCPWM_GENO_A_NCIFORCE_MODE, etc., with bit positions marked from 16 to 0. Bit values are shown for reset state (e.g., 0x20 at bit 5).)

```markdown
MCPWM_GENO_CNTUFORCE_UPMETHOD Configures update method for continuous software force of PWM generator0.

When all bits are set to 0: Immediately

When bit0 is set to 1: TEZ

When bit1 is set to 1: TEP

When bit2 is set to 1: TEA

When bit3 is set to 1: TEB

When bit4 is set to 1: Sync

When bit5 is set to 1: Disable update

TEA/B means an event generated when the timer’s value equals to that of register A/B.
(R/W)

MCPWM_GENO_A_CNTUFORCE_MODE Configures continuous software force mode for PWMOA.

0: Disabled
1: Low
2: High
3: Disabled
(R/W)

MCPWM_GENO_B_CNTUFORCE_MODE Configures continuous software force mode for PWMOB.
See details in MCPWM_GENO_A_CNTUFORCE_MODE. (R/W)

MCPWM_GENO_A_NCIFORCE Configures whether or not to trigger a non-continuous immediate software-force event for PWMOA.

0: No effect
1: Trigger a force event
(R/W)

MCPWM_GENO_A_NCIFORCE_MODE Configures non-continuous immediate software force mode for PWMOA.

0: Disabled
1: Low
2: High
3: Disabled
(R/W)
```

Continued on the next page...

Espressif Systems

1245 ESP32-C6 TRM (Version 1.1)

Submit Documentation Feedback
```