**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**

- **PWM timer:** 
  - Period = 6

- **Labels for different sections of the diagram from top to bottom:**
  - A = 3, B = 5
  
- **Sections labeled as follows with corresponding waveforms:**
  - UTEP
  - UTEZ
  - UTEA
  - UTEB

- **PWMx labels for different lines at the base of each waveform section from left to right are marked by arrows pointing upwards and downwards.**

**Figure Caption:** 
"Figure 36.3-15. Count-Up, Single Edge Asymmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High"

**Equation:**
```
Period = (MCPWM_TIMERx PERIOD + 1) x TPT.clk
```

**Text Explanation Below Diagram:** 
"The duty modulation for PWMxA is set by B, active high and proportional to B.
The duty modulation for PWMxB is set by A, active high and proportional to A."

**Footer:**
- "Espressif Systems"
- Page number 1344
- Document version ESP32-S3 TRM (Version 1.7)
- Links/Options:
  - Submit Documentation Feedback