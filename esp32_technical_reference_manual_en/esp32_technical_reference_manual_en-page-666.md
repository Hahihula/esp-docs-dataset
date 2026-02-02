**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**
- **PWM timer**: A graphical representation showing a count-up-down waveform.
- **DTEP, UTEZ, UTEA, DTEA, UTEB, DTEB**: These labels correspond to different sections of the diagram indicating specific points or states in the PWM signal.

**Figure Caption:**
"Figure 29.3-18. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Complementary"

**Body Text Explanation:**
The duty modulation of PWMxA is set by A, is active high and proportional to A.
The duty modulation of PWMxB is set by B, is active low and proportional to B.

Outputs PWMx can drive upper/lower (complementary) switches. Dead-time = B - A; Edge placement is fully programmable by software. Use the dead-time generator module if another edge delay method is required.

**Equation:**
Period = (2 × PWM_TIMER PERIOD + 1) × TPT_CLK

**Footer Information:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)

**Navigation Link:**
GoBack