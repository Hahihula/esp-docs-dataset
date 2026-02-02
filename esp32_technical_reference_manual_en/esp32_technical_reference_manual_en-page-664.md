**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Diagram Description and Labels:**
- **PWM timer**: 
  - Period = 6
  - A = 3
  - B = 5

- Waveforms labeled as:
  - UTEP, UTEZ, UTEA, UTEB
  
- Count-Up Pulse Placement Asymmetric Waveform with Independent Modulation on PWMxA and PWMxB.

**Equation:**
\[ \text{Period}d = (\text{PWM}_\text{TIMER}_x \cdot \text{PERIOD} + 1) \times T_{clk} \]

**Caption for Diagram:**
Figure 29.3-16. Count-Up, Pulse Placement Asymmetric Waveform with Independent Modulation on PWMxA and PWMxB

**Additional Information:**
Pulses may be generated anywhere within the PWM cycle (zero – period).
PWMxA’s high time duty is proportional to (\( B - A \)).

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback