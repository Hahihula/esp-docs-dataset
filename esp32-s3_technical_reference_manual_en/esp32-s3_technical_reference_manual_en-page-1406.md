**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Register Information:**
- **Register Name:** MCPWM_INT_ENA_REG (0x110)
- **Address Bits:** Reserving bits from the address for various interrupt enable registers.

**Interrupt Enable Registers and Descriptions:**

1. **MCPWM_TIMERO_STOP_INTENA**
   - Description: The enable bit for the interrupt triggered when the timer 0 stops.
   - Access Type: (R/W)

2. **MCPWM_TIMER1_STOP_INTENA**
   - Description: The enable bit for the interrupt triggered when the timer 1 stops.
   - Access Type: (R/W)

3. **MCPWM_TIMER2_STOP_INTENA**
   - Description: The enable bit for the interrupt triggered when the timer 2 stops.
   - Access Type: (R/W)

4. **MCPWM_TIMERO_TEZ_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 0 TEZ event.
   - Access Type: (R/W)

5. **MCPWM_TIMER1_TEZ_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 1 TEZ event.
   - Access Type: (R/W)

6. **MCPWM_TIMER2_TEZ_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 2 TEZ event.
   - Access Type: (R/W)

7. **MCPWM_TIMERO_TEP_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 0 TEP event.
   - Access Type: (R/W)

8. **MCPWM_TIMER1_TEP_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 1 TEP event.
   - Access Type: (R/W)

9. **MCPWM_TIMER2_TEP_INTENA**
   - Description: The enable bit for the interrupt triggered by a PWM timer 2 TEP event.
   - Access Type: (R/W)

10. **MCPWM_FAULTO_INTENA**
    - Description: The enable bit for the interrupt triggered when event_f0 starts.
    - Access Type: (R/W)

11. **MCPWM_FAULT1_INTENA**
    - Description: The enable bit for the interrupt triggered when event_f1 starts.
    - Access Type: (R/W)

12. **MCPWM_FAULT2_INTENA**
    - Description: The enable bit for the interrupt triggered when event_f2 starts.
    - Access Type: (R/W)

13. **MCPWM_FAULTO_CLR_INTENA**
    - Description: The enable bit for the interrupt triggered when event_f0 ends.
    - Access Type: (R/W)

**Footer Information:**
- Continued on the next page...
- Page Number and Document Version:
  - "Espressif Systems"
  - "1406 ESP32-S3 TRM (Version 1.7)"
- Submission Link for Documentation Feedback

**Diagram Description:** 
The image includes a bit map showing various interrupt enable registers, with each register labeled by its name followed by the corresponding address bits in hexadecimal format.

**Bit Map Details:**
- The diagram shows addresses from `0x110` to `0x120`, indicating different interrupt enable settings for various PWM timer events and faults. Each bit is associated with a specific function, such as stopping or triggering an event on the timers (e.g., TIMERO, TIMER1, TIMER2) or handling fault conditions.

**Note:** The diagram provides visual representation of how each register's bits are mapped to different interrupt triggers in the MCPWM module for efficient hardware control and monitoring.