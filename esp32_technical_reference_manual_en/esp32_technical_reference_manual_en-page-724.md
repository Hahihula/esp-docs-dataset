**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Heading:**
Register 29.71. INT_ST_PWM_REG (0x0118)

**Continuation Note:**
Continued from the previous page...

**List of Interrupt Status Bits with Descriptions and Access Mode:**

- **INT_FAULT1_INT_ST**: The masked status bit for the interrupt triggered when event_f1 starts.
  - Access mode: Read/Only (RO)
  
- **INT_FAULT0_INT_ST**: The masked status bit for the interrupt triggered when event_f0 starts.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER2_TEP_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 2 TEP event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER1_TEP_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 1 TEP event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMERO_TEP_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 0 TEP event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER2_TEZ_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 2 TEZ event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER1_TEZ_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 1 TEZ event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMERO_TEZ_INT_ST**: The masked status bit for the interrupt triggered by a PWM timer 0 TEZ event.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER2_STOP_INT_ST**: The masked status bit for the interrupt triggered when the timer 2 stops.
  - Access mode: Read/Only (RO)
  
- **INT_TIMER1_STOP_INT_ST**: The masked status bit for the interrupt triggered when the timer 1 stops.
  - Access mode: Read/Only (RO)
  
- **INT_TIMERO_STOP_INT_ST**: The masked status bit for the interrupt triggered when the timer 0 stops.
  - Access mode: Read/Only (RO)

**Footer Information:**
Espressif Systems
Page number: 724
Document version and type information at bottom right corner.