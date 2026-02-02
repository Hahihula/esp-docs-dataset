**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Register Section Titles and Descriptions with Binary Representation:**

1. **PWM_TIMER2_STATUS_REG (0x0030)**
   - **PWM_TIMER2_DIRECTION**: Current direction of the PWM timer2 count. 0: increment, 1: decrement.
     - Binary representation shown.

2. **PWM_TIMER2_VALUE**:
   - Current value of the PWM timer2 counter.
   - Binary representation and reset option indicated (Reset).

3. **PWM_TIMER_SYNCI_CFG_REG (0x0034)**
   - Multiple fields with descriptions for each bit position, including:
     1. **PWM_EXTERNAL_SYNCI2_INVERT**: Invert SYNC2 from GPIO matrix.
        - Binary representation shown.

     2. **PWM_EXTERNAL_SYNCI1_INVERT** and others: Similar structure to the above field but different inversion points (e.g., SYNC1).

     3. **PWM_TIMER2_SYNCISEL**: Select sync input for PWM timer2 with various options:
        - Binary representation showing multiple fields.
        
     4. **PWM_TIMER1_SYNCISEL** and other similar sections: Similar structure to the above field but different timer references (e.g., timer0).

5. **PWM_TIMERO_SYNCISEL**: Select sync input for PWM timer0.

---

**Footer Information:** 
- Page number at bottom center.
- Company name "Espressif Systems".
- Document version and type information on right side: ESP32 TRM (Version 5.6).
- Submission link labeled as “Submit Documentation Feedback”.