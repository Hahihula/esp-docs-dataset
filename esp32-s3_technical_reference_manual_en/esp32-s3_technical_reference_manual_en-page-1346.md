**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**

- **PWM timer:** 
  - Period = 6

- **Count-Up/Down, Dual Edge Symmetric Waveform with Independent Modulation on PWMxA and PWMxB — Active High.**

- **Labels for the diagram include:**
  - A = 3
  - B = 5
  
- **Waveforms labeled as follows from top to bottom:** 
  - DTEP (0,1,2,...)
  - UTEZ
  - UTEA
  - DTEA
  - UTEB
  - DTEB

- **PWMxA and PWMxB:**
  - Two lines indicating the duty modulation for each.

**Equation at bottom of diagram:** 
Period = (2 × MCPWM_TIMERRXPERIOD) × TPT_CLK

**Text below Diagram Explanation:**

The duty modulation for PWMxA is set by A, active high and proportional to A.
The duty modulation for PWMxB is set by B, active high and proportional to B.

Outputs PWMxA and PWMxB can drive independent switches. 

**Footer Information:** 
Espressif Systems
1346 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link:**
GoBack