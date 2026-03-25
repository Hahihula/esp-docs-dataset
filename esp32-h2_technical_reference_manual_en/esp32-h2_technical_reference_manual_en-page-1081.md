

```markdown
Chapter 36 Motor Control PWM (MCPWM)
GoBack

Figure 36.3-22 shows a waveform of CNTU software-force events. UTEZ events are selected as triggers for CNTU software-force events. CNTU is used to force the PWMxB output low. Forcing on PWMxA is disabled.

Period = 6
A = 3

PWM timer

UTEP

UTEZ

UTEA

CNTU force event

PWMxA

CNTU force mode on PWMxB   force low    disable

PWMxB

Figure 36.3-22. Example of a CNTU Software-Force Event on PWMxB
```