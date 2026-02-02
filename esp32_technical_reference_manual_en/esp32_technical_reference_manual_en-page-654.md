**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Note Section:**
- Note: The period register is PWM_TIMERx.PERIOD (x = 0, 1, 2), i.e., PWM_TIMERO.PERIOD, PWM_TIMER1.PERIOD, PWM_TIMER2.PERIOD.

**Subsections and Descriptions:**

1. **Count-Down Mode:**
   - Description:
     "The PWM timer decrements to zero, starting from the value configured in the period register. After reaching zero, it is set back to the period value. Then it starts to decrement again. In this case, the PWM period is also equal to the value of period register + 1."

2. **Count-Up-Down Mode:**
   - Description:
     "This is a combination of the two modes mentioned above. The PWM timer starts increasing from zero until the period value is reached. Then, the timer decreases back to zero. This pattern is then repeated. The PWM period is the result (the value of period register x 2 + 1)."

**Figures Section:**
- Figures are referenced as "Figures 29.3-6 to 29.3-9 show PWM timer waveforms in different modes, including timer behavior during synchronization events."

**Diagrams and Captions:**

1. **Figure Caption (Count-Up Mode Waveform):**
   - Title: Figure 29.3-6.
   - Description:
     "Count-Up Mode Waveform"

2. **Figure Caption (Count-Down Mode Waveforms):**
   - Title: Figure 29.3-7.

**Footer Information:**
- Company Name and Document Version Info
  - Espressif Systems
  - Page Number: 654
  - Document Type: ESP32 TRM (Version 5.6)
  - Submit Documentation Feedback Link

(Note: The actual waveforms in the images are not described as they contain graphical information.)