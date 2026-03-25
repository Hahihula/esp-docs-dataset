

```markdown\nPeriod = 6  \nPWM timer  \nUTEP  \nUTEZ  \nUTEA  \nUTEB  \nPWMxA  \nPWMxB  \n```\n\nFigure 36.3-17. Count-Up, Pulse Placement Asymmetric Waveform with Independent Modulation on PWMxA\n\nPulses may be generated anywhere within one PWM cycle (zero to period).  \nPWMxA’s high-time duty is proportional to (B – A).\n\nPeriod = (MCPWM_TIMERx_PERIOD + 1) × TPT_CLK
```