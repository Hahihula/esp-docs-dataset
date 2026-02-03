**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Number and Name:**
36.4 Register Summary

**Body Text:**
The addresses in this section are relative to Motor Control PWM0 and Motor Control PWM1 base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers (Column Titles):**
- Name
- Description
- Address
- Access

**Table Content:**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Prescaler configuration | PWM clock prescaler register | 0x0000 | R/W |
| PWM Timer 0 Configuration and status | PWM timer0 period and update method configuration register | 0x0004 | R/W |
| MCPWM_TIMERO_CFG0_REG | PWM timer0 working mode and start/stop control configuration register | 0x0008 | R/W |
| MCPWM_TIMERO_SYNC_REG | PWM timer0 sync function configuration register | 0x0010 | RO |
| MCPWM_TIMERO_STATUS_REG | PWM timer0 status register | varies | - |
| PWM Timer 1 Configuration and Status | PWM timer1 period and update method configuration register | 0x0014 | R/W |
| MCPWM_TIMER1_CFG0_REG | PWM timer1 working mode and start/stop control configuration register | 0x0018 | RO |
| MCPWM_TIMER1_SYNC_REG | PWM timer1 sync function configuration register | 0x001C | R/W |
| MCPWM_TIMER1_STATUS_REG | PWM timer1 status register | varies | - |
| PWM Timer 2 Configuration and Status | PWM timer2 period and update method configuration register | 0x0024 | R/W |
| MCPWM_TIMER2_CFG0_REG | PWM timer2 working mode and start/stop control configuration register | 0x0028 | RO |
| MCPWM_TIMER2_SYNC_REG | PWM timer2 sync function configuration register | varies | - |
| MCPWM_TIMER2_STATUS_REG | PWM timer2 status register | 0x0030 | R/W |
| Common configuration for PWM timers | Synchronization input selection for three PWM timers | 0x0034 | RO |
| MCPWM OPERATOR_TIMERSSEL_REG | Select specific timer for PWM operators | varies | - |
| PWM Operator O Configuration and Status | Transfer status and update method for time stamp registers A and B | 0x003C | R/W |
| MCPWM_GENO_STMP_CFG_REG | PWM generator O shadow register for timer stamp A | 0x0040 | RO |
| MCPWM_GENO_TSTMP_A_REG | PWM generator O event TO handling | varies | - |
| MCPWM_GENO_STMP_B_REG | PWM generator O shadow register for timer stamp B | 0x0044 | R/W |
| MCPWM_GENO_CFGO_REG | PWM generator O event TO and T1 handling | 0x0048 | RO |

**Footer:**
Espressif Systems  
Page number (centered): 1361  
Document version information at the bottom right corner.