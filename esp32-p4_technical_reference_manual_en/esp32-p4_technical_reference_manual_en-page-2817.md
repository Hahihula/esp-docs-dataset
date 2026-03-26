

```markdown
Chapter 56 Motor Control PWM (MCPWM)

Figure 56.3-14. Count-Up, Single Edge Asymmetric Waveform, with Independent Modulation on PWMxA and PWMxB — Active High

The duty modulation for PWMxA is set by B, active high and proportional to B.
The duty modulation for PWMxB is set by A, active high and proportional to A.

Period = (MCPWM_TIMERn_PERIOD + 1) × TPT_clk
```