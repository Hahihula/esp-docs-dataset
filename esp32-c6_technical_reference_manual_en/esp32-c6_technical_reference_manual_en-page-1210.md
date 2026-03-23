

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

Figure 36.3-17. Count-Up, Pulse Placement Asymmetric Waveform with Independent Modulation on PWMxA

Pulses may be generated anywhere within the PWM cycle (zero to period).

PWMxA's high time duty is proportional to (B - A).

Period = (MCPWM_TIMERx_PERIOD + 1) × TPT_clk
```