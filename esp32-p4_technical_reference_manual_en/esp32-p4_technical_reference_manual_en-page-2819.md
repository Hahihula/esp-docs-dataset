

```markdown
Chapter 56 Motor Control PWM (MCPWM)                                                                 GoBack


Period = 6
A = 3
B = 5

PWM timer

DTEP

UTEZ

UTEA

DTEA

UTEB

DTEB

PWMxA

PWMxB


Figure 56.3-16. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High

The duty modulation for PWMxA is set by A, active high and proportional to A.
The duty modulation for PWMxB is set by B, active high and proportional to B.
Outputting PWMxA and PWMxB can drive separate switches.

Period = (2 × MCPWM_TIMERn_PERIOD) × TPT_clk


Espressif Systems          2819                  ESP32-P4 TRM
Submit Documentation Feedback               PRELIMINARY
```