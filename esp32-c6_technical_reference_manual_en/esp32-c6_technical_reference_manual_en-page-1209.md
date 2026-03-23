

```markdown
Chapter 36 Motor Control PWM (MCPWM) GoBack


Period = 6
A = 3
B = 5

PWM timer

UTEP

UTEZ

UTEA

UTEB

PWMxA

PWMxB

Figure 36.3-16. Count-Up, Single Edge Asymmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High


The duty modulation for PWMxA is set by B, active high and proportional to B.
The duty modulation for PWMxB is set by A, active high and proportional to A.

Period = (MCPWM_TIMERx_PERIOD + 1) × TPT_clk

Espressif Systems
1209
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```