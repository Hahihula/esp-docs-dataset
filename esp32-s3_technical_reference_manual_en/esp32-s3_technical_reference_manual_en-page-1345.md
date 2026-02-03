**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**
- **PWM timer**: 
  - Period = 6, A = 3, B = 5

- Waveforms labeled as:
  - UTEP
  - UTEZ
  - UTEA
  - UTEB
  
- Independent Modulation on PWMxA (labeled T) and PWMxB.

**Figure Caption:**
Figure 36.3-16. Count-Up, Pulse Placement Asymmetric Waveform with Independent Modulation on PWMxA

**Equation Description:**
Period = ((MCPWM_TIMERxPERIOD + 1) x TPT.clk)

**Additional Information:**
Pulses may be generated anywhere within the PWM cycle (zero – period).
PWMxA’s high time duty is proportional to (B - A).

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback