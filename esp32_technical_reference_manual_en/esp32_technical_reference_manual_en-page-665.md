**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**

- **PWM timer:** 
  - Period = 6

- **Count-Up, Down, Dual Edge Symmetric Waveform with Independent Modulation on PWMxA and PWMxB — Active High.**

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
  - Indicated with arrows pointing downwards.

**Equation for Period Calculation:** 
Period = (2 × PWM_TIMERx PERIOD + 1) × TPT_clk

**Text Explanation under Diagrams:**

The duty modulation for PWMxA is set by A, active high and proportional to A.
The duty modulation for PWMxB is set by B, active high and proportional to B.

Outputs PWMxA and PWMxB can drive independent switches. 

**Footer Information:** 
Espressif Systems
665 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack