**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.71. MCPWM_INT_ST_REG (0x118)

**Body Text with Descriptions of Registers and Their Functions:**

Continued from the previous page...

- **MCPWM_FAULT1_CLR_INT_ST**: The masked status bit for the interrupt triggered when event_f1 ends.
  - (RO)
  
- **MCPWM_FAULT2_CLR_INT_ST**: The masked status bit for the interrupt triggered when event_f2 ends.
  - (RO)

- **MCPWM_OPO_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 0 TEA event
  - (RO)
  
- **MCPWM_OP1_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 1 TEA event
  - (RO)

- **MCPWM_OP2_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 2 TEA event
  - (RO)
  
- **MCPWM_OPO_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 0 TEB event
  - (RO)

- **MCPWM_OP1_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 1 TEB event
  - (RO)

- **MCPWM_OP2_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 2 TEB event
  - (RO)
  
- **MCPWM_FHO_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM0.
  - (RO)

- **MCPWM_FH1_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM1
  - (RO)
  
- **MCPWM_FH2_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM2.
  - (RO)

- **MCPWM_FHO_OST_INT_ST**: The masked status bit for the interrupt triggered by a one-shot mode action on PWM0
  - (RO)
  
- **MCPWM_FH1_OST_INT_ST**: The masked status bit for the interrupt triggered by a one-shot mode action on PWM1.
  - (RO)

- **MCPWM_FH2_OST_INT_ST**: The masked status bit for the interrupt triggered by a one-shot mode action on PWM2
  - (RO)
  
- **MCPWMCAPEOINTST**: The masked status bit for the interrupt triggered by capture on channel 0.
  - (RO)

- **MCPWMCAP1INTST**: The masked status bit for the interrupt triggered by capture on channel 1.
  - (RO)

- **MCPWMCAP2INTST**: The masked status bit for the interrupt triggered by capture on channel 2
  - (RO)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)