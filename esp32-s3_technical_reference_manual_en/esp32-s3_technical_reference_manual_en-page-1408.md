**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Header:**
Register 36.70. MCPWM_INT_RAW_REG (0x114)

**Table Header Row:**
- MCPWM_CAP2_INT_RAW
- MCPWM_CAP0_INT_RAW
- MCPWM_FIH02_INT_RAW
- MCPWM_FIH01_INT_RAW
- MCPWM_FIH00_INT_RAW
- MCPWM_OPI0_TEA_INT_RAW
- MCPWM_OPI0_TEZ_INT_RAW
- MCPWM_OPI0_TEP_INT_RAW
- MCPWM_OPI0_TEP2_INT_RAW
- MCPWM_OPI0_TEP3_INT_RAW
- MCPWM_OPI0_TEP4_INT_RAW
- MCPWM_OPI0_TEP5_INT_RAW
- MCPWM_OPI0_TEP6_INT_RAW
- MCPWM_OPI0_TEP7_INT_RAW
- MCPWM_OPI0_TEZ2_INT_RAW
- MCPWM_OPI0_TEZ3_INT_RAW
- MCPWM_OPI0_TEZ4_INT_RAW
- MCPWM_OPI0_TEZ5_INT_RAW

**Table Row:**
- 31 (reserved)
- 30 to 0, all zeros.

**Footer Note:** 
Reset

**List of Interrupt Status Bits and Descriptions with Access Type Indicators R/WTC/SS or SS only for read access**

- **MCPWM_TIMER0_STOP_INT_RAW**: The raw status bit for the interrupt triggered when the timer 0 stops. (R/WTC/SS)
- **MCPWM_TIMER1_STOP_INT_RAW**: The raw status bit for the interrupt triggered when the timer 1 stops. (R/WTC/SS)
- **MCPWM_TIMER2_STOP_INT_RAW**: The raw status bit for the interrupt triggered when the timer 2 stops. (R/WTC/SS)
- **MCPWM_TIMER0_TEZ_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 0 TEZ event. (R/WTC/SS)
- **MCPWM_TIMER1_TEZ_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 1 TEZ event. (R/WTC/SS)
- **MCPWM_TIMER2_TEZ_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 2 TEZ event. (R/WTC/SS)
- **MCPWM_TIMER0_TEP_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 0 TEP event. (R/WTC/SS)
- **MCPWM_TIMER1_TEP_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 1 TEP event. (R/WTC/SS)
- **MCPWM_TIMER2_TEP_INT_RAW**: The raw status bit for the interrupt triggered by a PWM timer 2 TEP event. (R/WTC/SS)
- **MCPWM_FAULT0_INT_RAW**: The raw status bit for the interrupt triggered when event_f0 starts. (R/WTC/SS)
- **MCPWM_FAULT1_INT_RAW**: The raw status bit for the interrupt triggered when event_f1 starts. (R/WTC/SS)
- **MCPWM_FAULT2_INT_RAW**: The raw status bit for the interrupt triggered when event_f2 starts. (R/WTC/SS)
- **MCPWM_FAULT0_CLR_INT_RAW**: The raw status bit for the interrupt triggered when event_f0 ends. (R/WTC/SS)

**Continuation Note:**
Continued on the next page...

**Footer Information:** 
Espressif Systems
1408 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback