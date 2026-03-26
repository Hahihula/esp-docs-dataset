

```markdown
Chapter 56 Motor Control PWM (MCPWM)                                                                 GoBack


Period = 6
A = 3
B = 4
up-count mode

PWM timer

DTEP

UTEZ

UTEA

DTEA

UTEB

DTEB

PWMxA

PWMxB


Figure 56.3-17. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Complementary

The duty modulation of PWMxA is set by A, is active high and proportional to A.
The duty modulation of PWMxB is set by B, is active low and proportional to B.
Outputs PWMx can drive upper/lower (complementary) switches.
Dead time = B – A. Edge placement is configurable by software. Dead time generator module supports configuring edge delay methods when required.

Period = (2 × MCPWM_TIMERn_PERIOD) × TPT_clk


Espressif Systems          2820
Submit Documentation Feedback        ESP32-P4 TRM
PRELIMINARY
```