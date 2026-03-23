

```markdown\nPeriod = 6\nA = 3\nB = 5\nPWM timer\nDTEP\nUTEZ\nUTEA\nDTEA\nUTEB\nDTEB\nPWMxA\nPWMxB\nFigure 36.3-18. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High\nThe duty modulation for PWMxA is set by A, active high and proportional to A.\nThe duty modulation for PWMxB is set by B, active high and proportional to B.\nOutputting PWMxA and PWMxB can drive separate switches.\nPeriod = (2 × MCPWM_TIMERx_PERIOD) × TPT_clk\n```
```markdown
Chapter 36 Motor Control PWM (MCPWM)
GoBack

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

Figure 36.3-18. Count-Up-Down, Dual Edge Symmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High

The duty modulation for PWMxA is set by A, active high and proportional to A.
The duty modulation for PWMxB is set by B, active high and proportional to B.
Outputting PWMxA and PWMxB can drive separate switches.

Period = (2 × MCPWM_TIMERx_PERIOD) × TPT_clk
```