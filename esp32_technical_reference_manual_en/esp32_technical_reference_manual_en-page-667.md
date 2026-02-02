**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Link:**
GoBack

**Subtitle: Software-Force Events**

**Body Text:**
There are two types of software-force events inside the PWM generator:

1. **Non-continuous-immediate (NCI) software-force events**: Such types of events are immediately effective on PWM outputs when triggered by software. The forcing is non-continuous, meaning the next active timing events will be able to alter the PWM outputs.

2. **Continuous (CNTU) software-re-force events**: Such types of events are continuous. The forced PWM outputs will continue until they are released by software. The events' triggers are configurable. They can be timing events or immediate events.

**Figure Caption:**
Figure 29.3-19 shows a waveform of NCI software-force events. NCI events are used to force PWMxA output low. Forcing on PWMxB is disabled in this case.
```
Period = 6
A = 3

PWM timer
0   1   2   3   4   5   6

UTEP
UTEZ
UTEA

NCI force event
PWMxA
PWMxB
```

**Figure Caption:**
Figure 29.3-20 shows a waveform of CNTU software-force events. UTEZ events are selected as triggers for Espressif Systems.

**Footer Information:**
667 ESP32 TRM (Version 5.6)
Submit Documentation Feedback