

```markdown
Chapter 41 Motor Control PWM (MCPWM) GoBack

Period = 6
A = 3
B = 5

PWM timer

UTEP

UTEZ

UTEA

UTEB

PWMxA

PWMxB — Active High

Figure 41.3-14. Count-Up, Single Edge Asymmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High

The duty modulation for PWMxA is set by B, active high and proportional to B.
The duty modulation for PWMxB is set by A, active high and proportional to A.

Period = (MCPWM_TIMERn_PERIOD + 1) × TPT_clk
```