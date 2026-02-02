**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Back Navigation Link:** GoBack

**Register Information Table Header:**
- Register Name and Offset
- Description of the register's function or purpose.

**Table Content for PWM GEN2 Registers:**

| **Register Number/Name** | **Description** |
|---------------------------|------------------|
| PWM_GEN2_B_NCIFORCE_MODE | Non-continuous immediate software-force mode for PWM2B, 0: disabled, 1: low, 2: high, 3: disabled. (R/W) |
| PWM_GEN2_B_NCIFORCE | Trigger of non-continuous immediate software-force event for PWM2B, a toggle will trigger a force event. (R/W) |
| PWM_GEN2_A_NCIFORCE_MODE | Non-continuous immediate software-force mode for PWM2A, 0: disabled, 1: low, 2: high, 3: disabled. (R/W) |
| PWM_GEN2_A_NCIFORCE | Trigger of non-continuous immediate software-force event for PWM2A, a toggle will trigger a force event. (R/W) |
| PWM_GEN2_B_CNTUFORCE_MODE | Continuous software-force mode for PWM2B, 0: disabled, 1: low, 2: high, 3: disabled. (R/W) |
| PWM_GEN2_A_CNTUFORCE_MODE | Continuous software-force mode for PWM2A, 0: disabled, 1: low, 2: high, 3: disabled. (R/W) |
| PWM_GEN2_CNTUFORCE_UPMETHOD | Updating method for continuous software force of PWM generator2; 0: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: TEA; when bit3 is set to 1: TEB; when bit4 is set to 1: sync; when bit5 is set to 1: disable update. (TEA/B here and below means an event generated when the timer value equals that of register A/B.) (R/W) |

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version: ESP32 TRM (Version 5.6)
- Page Number: 707

**Navigation Links at Bottom:** Submit Documentation Feedback