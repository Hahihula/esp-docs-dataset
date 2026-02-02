**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description with Labels and Annotations:**

- **PWM timer:** 
  - Period = 6

- **Count-Up, Single Edge Asymmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High.**

- **PWMxA**
- **PWMxB**

**Equation for Duty Modulation:**
\[ \text{Period} = (\text{PWM_TIMERx}_\text{-PERIOD} + 1) \times T_{P\_clk} \]

**Explanation of Duty Modulation Proportional Relationship (Text below the diagram):**
- The duty modulation for PWMxA is set by B, active high and proportional to B.
- The duty modulation for PWMxB is set by A, active high and proportional to A.

**Footer:**
Espressif Systems
663 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:** 
GoBack