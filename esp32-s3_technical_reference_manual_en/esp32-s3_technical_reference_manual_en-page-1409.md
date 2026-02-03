**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Header:**
Register 36.70, MCPWM_INT_RAW_REG (0x114)

**Body Text:**

Continued from the previous page...

- **MCPWM_FAULT1_CLR_INT_RAW**: The raw status bit for the interrupt triggered when event_f1 ends.
  - (R/WTC/SS)
  
- **MCPWM_FAULT2_CLR_INT_RAW**: The raw status bit for the interrupt triggered when event_f2 ends.
  - (R/WTC/SS)

- **MCPWM_OPO_TEA_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 0 TEA event
  - (R/WTC/SS)
  
- **MCPWM_OP1_TEA_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 1 TEA event
  - (R/WTC/SS)

- **MCPWM_OP2_TEA_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 2 TEA event
  - (R/WTC/SS)
  
- **MCPWM_OPO_TEB_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 0 TEB event
  - (R/WTC/SS)

- **MCPWM_OP1_TEB_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 1 TEB event
  - (R/WTC/SS)
  
- **MCPWM_OP2_TEB_INT_RAW**: The raw status bit for the interrupt triggered by a PWM operator 2 TEB event
  - (R/WTC/SS)

- **MCPWM_FHO_CBC_INT_RAW**: The raw status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM0.
  - (R/WTC/SS)
  
- **MCPWM_FH1_CBC_INT_RAW**: The raw status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM1
  - (R/WTC/SS)

- **MCPWM_FH2_CBC_INT_RAW**: The raw status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM2.
  - (R/WTC/SS)
  
- **MCPWM_FHO_OST_INT_RAW**: The raw status bit for the interrupt triggered by a one-shot mode action on PWM0
  - (R/WTC/SS)

- **MCPWM_FH1_OST_INT_RAW**: The raw status bit for the interrupt triggered by a one-shot mode action on PWM1.
  - (R/WTC/SS)
  
- **MCPWM_FH2_OST_INT_RAW**: The raw status bit for the interrupt triggered by a one-shot mode action on PWM2
  - (R/WTC/SS)

- **MCPWMCAPEO_INT_RAW**: The raw status bit for the interrupt triggered by capture on channel 0.
  - (R/WTC/SS)
  
- **MCPWM_CAP1_INT_RAW**: The raw status bit for the interrupt triggered by capture on channel 1
  - (R/WTC/SS)

- **MCPWM_CAP2_INT_RAW**: The raw status bit for the interrupt triggered by capture on channel 2.
  - (R/WTC/SS)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)