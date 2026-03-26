

```markdown
Chapter 56 Motor Control PWM (MCPWM)    GoBack


Period = 6
A = 3
B = 5

PWM timer

UTEP

UTEZ

UTEA

UTEB

PWMAxA

PWMBxB


Figure 56.3-15. Count-Up, Pulse Placement Asymmetric Waveform with Independent Modulation on PWMAxA

Pulses may be generated anywhere within the PWM cycle (zero to period).
PWMAxA's high time duty is proportional to (B - A).

Period = (MCPWM_TIMERn_PERIOD + 1) × TPT_clk


Espressif Systems    2818
Submit Documentation Feedback    ESP32-P4 TRM
PRELIMINARY
```