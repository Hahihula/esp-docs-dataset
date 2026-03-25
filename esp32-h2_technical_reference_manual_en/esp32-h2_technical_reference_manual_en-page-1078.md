

```markdown
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

Figure 36.3-19. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Complementary
```

The duty modulation of `PWMxA` is set by A, is active high and proportional to A.
The duty modulation of `PWMxB` is set by B, is active low and proportional to B.
Outputs `PWMx` can drive upper/lower (complementary) switches.
Dead time = B – A. Edge placement is configurable by software. The dead time generator module supports configuring edge delay methods when required.

```math
Period = (2 × MCPWM_TIMERx_PERIOD) × TPT_CLK
```

Figure 36.3-20 shows a waveform when UTO/1 and DTO/1 events are generated. In this example, TO selects

Espressif Systems
1078
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```