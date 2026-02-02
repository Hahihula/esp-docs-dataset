**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information:**
- Register Number: 29.20, Name: PWM_GENO FORCE REG (0x004c)
- Bit Positions and Labels:
  - 31 to 8 are labeled as various modes for different channels.
  
**Table of Modes with Descriptions:**

| Mode | Description |
|------|-------------|
| **PWM_GENO_B_NCIFORCE_MODE** | Non-continuous immediate software-force mode for PWM0B. <br> Values: 0: disabled, 1: low, 2: high, 3: disabled (R/W) |
| **PWM_GENO_B_NCIFORCE** | Trigger of non-continuous immediate software-force event for PWM0B; a toggle will trigger a force event. (R/W) |
| **PWM_GENO_A_NCIFORCE_MODE** | Non-continuous immediate software-force mode for PWM0A, <br> Values: 0: disabled, 1: low, 2: high, 3: disabled (R/W) |
| **PWM_GENO_A_NCIFORCE** | Trigger of non-continuous immediate software-force event for PWM0A; a toggle will trigger a force event. (R/W) |
| **PWM_GENO_B_CNTUFORCE_MODE** | Continuous software-force mode for PWM0B, <br> Values: 0: disabled, 1: low, 2: high, 3: disabled (R/W) |
| **PWM_GENO_A_CNTUFORCE_MODE** | Continuous software-force mode for PWM0A. <br> Values: 0: disabled, 1: low, 2: high, 3: disabled (R/W) |
| **PWM_GENO_CNTUFORCE_UPMETHOD** | Updating method for continuous software force of PWM generator0; <br> When all bits are set to 0 immediately; when bit0 is set to 1 TEZ; when bit1 is set to 1 TEP; when bit2 is set to 1 TEA; when bit3 is set to 1 TEB; when bit4 is set to 1 sync; <br> When bit5 is set to 1 disable update. (TEA/B here and below means an event generated when the timer’s value equals to that of register A/B.) (R/W) |

**Footer:**
- Company Name: Espressif Systems
- Document Version Information: ESP32 TRM (Version 5.6)
- Page Number: 689

**Link for Feedback:**
Submit Documentation Feedback