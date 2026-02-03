**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.72. MCPWM_INT_CLR_REG (0x11C)

**Continuation Note:**
Continued from the previous page...

**List of Interrupt Clear Registers with Descriptions and Event Types:**

- **MCPWM_FAULT0_CLR_INT_CLR:** Set this bit to clear the interrupt triggered when event_f0 ends.
  - (WT)
  
- **MCPWM_FAULT1_CLR_INT_CLR:** Set this bit to clear the interrupt triggered when event_f1 ends.
  - (WT)

- **MCPWM_FAULT2_CLR_INT_CLR:** Set this bit to clear the interrupt triggered when event_f2 ends.
  - (WT)

- **MCPWM_OPO_TEA_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator O TEA event
  - (WT)
  
- **MCPWM_OP1_TEA_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator 1 TEA event
  - (WT)

- **MCPWM_OP2_TEA_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator 2 TEA event
  - (WT)

- **MCPWM_OPO_TEB_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator O TEB event
  - (WT)

- **MCPWM_OP1_TEB_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator 1 TEB event
  - (WT)

- **MCPWM_OP2_TEB_INT_CLR:** Set this bit to clear the interrupt triggered by a PWM operator 2 TEB event
  - (WT)

- **MCPWM_FHO_CBC_INT_CLR:** Set this bit to clear the interrupt triggered by a cycle-by-cycle mode action on PWMO.
  - (WT)
  
- **MCPWM_FH1_CBC_INT_CLR:** Set this bit to clear the interrupt triggered by a cycle-by-cycle mode action on PWM1.
  - (WT)

- **MCPWM_FH2_CBC_INT_CLR:** Set this bit to clear the interrupt triggered by a cycle-by-cycle mode action on PWM2
  - (WT)

- **MCPWM_FHO_OST_INT_CLR:** Set this bit to clear the interrupt triggered by a one-shot mode action on PWMO.
  - (WT)
  
- **MCPWM_FH1_OST_INT_CLR:** Set this bit to clear the interrupt triggered by a one-shot mode action on PWM1
  - (WT)

- **MCPWM_FH2_OST_INT_CLR:** Set this bit to clear the interrupt triggered by a one-shot mode action on PWM2.
  - (WT)

- **MCPWMCAPEO_INT_CLR:** Set this bit to clear the interrupt triggered by capture on channel O
  - (WT)
  
- **MCPWM_CAP1_INT_CLR:** Set this bit to clear the interrupt triggered by capture on channel 1
  - (WT)

- **MCPWM_CAP2_INT_CLR:** Set this bit to clear the interrupt triggered by capture on channel 2.
  - (WT)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)