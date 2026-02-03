**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack**

---

**Body Text and Diagrams Description:**

- **Period = 4, DTEA = CLEAR, UTEA = SET**

- **PWM Timer Direction Chart with Cases:**  
  - Case 1:
    - A = 4, 0% Duty
    - PWMxA/PWMxB (Output waveform)
  - Case 2:
    - A = 3, 25% Duty
    - PWMxA/PWMxB (Output waveform)
  - Case 3:
    - A = 2, 50% Duty
    - PWMxA/PWMxB (Output waveform)
  - Case 4:
    - A = 1, 75% Duty
    - PWMxA/PWMxB (Output waveform)
  - Case 5:
    - A = 0, 100% Duty
    - PWMxA/PWMxB (Output waveform)

**Figure Caption:**
Figure 36.3-14. Symmetrical Waveform in Count-Up-Down Mode

**Body Text Explanation of Diagrams and Concepts:**  
If \(A\) matches the PWM timer value, then when the PWM timer is incrementing, the PWM output is pulled up; if A matches the PWM timer value while the PWM timer is decrementing, then the PWM output is pulled low.

The PWM waveforms in Figures 36.3-15 to 36.3-18 show some common PWM operator configurations.
The following conventions are used:
- Period \(A\) and B refer to values written in corresponding registers
- PWMxA and PWMxB are the output signals of PWM Operator x

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  

ESP32-S3 TRM (Version 1.7)