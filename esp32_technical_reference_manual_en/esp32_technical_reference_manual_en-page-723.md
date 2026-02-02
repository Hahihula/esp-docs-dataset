**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Subtitle:**
Register 29.71. INT_ST_PWM_REG (0x0118)

**Menu/Navigation Link:**
GoBack

**Body Text with Table and Descriptions of Interrupt Status Bits for Various Channels in the PWM Controller:**

- **INT_CAP2_INT_ST**: The masked status bit for the interrupt triggered by capture on channel 2. (RO)
- **INT_CAP1_INT_ST**: The masked status bit for the interrupt triggered by capture on channel 1. (RO)
- **INT_CAPO_INT_ST**: The masked status bit for the interrupt triggered by capture on channel 0. (RO)
- **INT_FH2_OST_INT_ST**: The masked status bit for the interrupt triggered by a one-shot mode action on PWM2. (RO)
- **INT_FH1_OST_INT_ST**: The masked status bit for the interrupt triggered by a one-shot mode action on PWM1. (RO)
- **INT_FHOcacacaca**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWMO.
- **INT_FH2_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM2.
- **INT_FH1_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWM1.
- **INT_FHO_CBC_INT_ST**: The masked status bit for the interrupt triggered by a cycle-by-cycle mode action on PWMO.
- **INT_OP2_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 2 TEB event. (RO)
- **INT_OP1_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 1 TEB event. (RO)
- **INT_OPO_TEB_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator O TEB event. (RO)
- **INT_OP2_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 2 TEA event. (RO)
- **INT_OP1_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator 1 TEA event. (RO)
- **INT_OPO_TEA_INT_ST**: The masked status bit for the interrupt triggered by a PWM operator O TEA event. (RO)
- **INT_FAULT2_CLR_INT_ST**: The masked status bit for the interrupt triggered when event_f2 ends.
- **INT_FAULT1_CLR_INT_ST**: The masked status bit for the interrupt triggered when event_f1 ends.
- **INT_FAULTO_CLR_INT_ST**: The masked status bit for the interrupt triggered when event_f0 ends.

**Continuation Note:**
Continued on the next page...

**Footer Information:**
Espressif Systems
Page number 723 (ESP32 TRM, Version 5.6)
Submit Documentation Feedback