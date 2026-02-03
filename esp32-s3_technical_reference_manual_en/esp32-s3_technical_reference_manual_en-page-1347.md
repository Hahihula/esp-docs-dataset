**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**
- **PWM timer**: 
  - Period = 6
  - A = 3
  - B = 4
  - up-count mode

- **Timers/Counters**:
  - DTEP, UTEZ, UTEA, DTEA, UTEB, DTEB
  
- **PWMx Registers**: 
  - PWMxA and PWMxB (labeled as complementary)

**Figure Caption:**
Figure 36.3-18. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Complementary

**Body Text Explanation of Diagrams Functions:**
The duty modulation of PWMxA is set by A, is active high and proportional to A.
The duty modulation of PWMxB is set by B, is active low and proportional to B.

Outputs PWMx can drive upper/lower (complementary) switches. Dead-time = B – A; Edge placement is fully programmable by software. Use the dead-time generator module if another edge delay method is required.

**Equation:**
Period = (2 × MCPWM_TIMERx_PERIOD) × TPTClk

**Footer Information:**
Espressif Systems
1347 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback