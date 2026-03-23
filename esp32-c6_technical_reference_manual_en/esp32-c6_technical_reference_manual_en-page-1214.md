

```markdown
Chapter 36 Motor Control PWM (MCPWM)    GoBack

be configured to be timing events or immediate events.

Figure 36.3-21 shows a waveform of NCI software-force events. NCI events are used to force PWMxA output low. Forcing on PWMxB is disabled in this case.

Period = 6
A = 3

PWM timer | UTEP | UTEZ | UTEA | NCI force event | PWMxA | PWMxB
---|---|---|---|---|---|---
(Steps 0-6) | (Waveform pulses) | (Waveform pulses) | (Waveform pulses) | (Rectangular pulses) | (Transitions with arrows) | (Transitions with arrows)

Figure 36.3-21. Example of an NCI Software-Force Event on PWMxA

Epressif Systems    1214    Submit Documentation Feedback    ESP32-C6 TRM (Version 1.1)
```