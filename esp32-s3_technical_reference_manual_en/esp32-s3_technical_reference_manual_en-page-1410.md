**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Header:**
Register 36.71. MCPWM_INT_ST_REG (0x0118)

**Table Description:**
- The table lists various interrupt status bits for different components of the MCPWM module.
- Each row represents a specific interrupt or event, with corresponding masked status bit positions in the register.

**List Items and Descriptions:**

1. **MCPWM_TIMERO_STOP_INTE_ST**
   - The masked status bit for the interrupt triggered when the timer 0 stops (RO).

2. **MCPWM_TIMER1_STOP_INTE_ST**
   - The masked status bit for the interrupt triggered when the timer 1 stops (RO).

3. **MCPWM_TIMER2_STOP_INTE_ST**
   - The masked status bit for the interrupt triggered when the timer 2 stops (RO).

4. **MCPWM_TIMERO_TEZ_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 0 TEZ event (RO).

5. **MCPWM_TIMER1_TEZ_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 1 TEZ event (RO).

6. **MCPWM_TIMER2_TEZ_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 2 TEZ event (RO).

7. **MCPWM_TIMERO_TEP_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 0 TEP event (RO).

8. **MCPWM_TIMER1_TEP_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 1 TEP event (RO).

9. **MCPWM_TIMER2_TEP_INTE_ST**
   - The masked status bit for the interrupt triggered by a PWM timer 2 TEP event (RO).

10. **MCPWM_FAULTO_INTE_ST**
    - The masked status bit for the interrupt triggered when event_f0 starts.

11. **MCPWM_FAULTI1_INTE_ST**
    - The masked status bit for the interrupt triggered when event_f1 starts.

12. **MCPWM_FAULTI2_INTE_ST**
    - The masked status bit for the interrupt triggered when event_f2 starts (RO).

13. **MCPWM_FAULTO_CLR_INTE_ST**
    - The masked status bit for the interrupt triggered when event_f0 ends (RO).

**Footer:**
Continued on the next page...

**Company Information and Document Details:**
Espressif Systems
Page 1410 of ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback