

```markdown
Period = 6
T0 = FAULT0
T1 = FAULT1

PWM timer

FAULT0

FAULT1

DT0

DT1

UT0

UT1

PWMA/B   T   T   T   T

Figure 41.3-18. Count-Up-Down, Fault or Synchronization Events, with Same Modulation on PWMxA and PWMxB
```

```markdown
Figure 41.3-18 shows a waveform when UTO/1 and DTO/1 events are generated. In this example, TO selects FAULT0 and T1 selects FAULT1. The events selected by TO and T1 can be configured independently; these events can be FAULT0, FAULT1, FAULT2 or synchronous. For detailed configuration, see section 41.3.3.1.
```

```markdown
Software-Force Events

There are two types of software-force events inside the PWM generator:

*   Non-continuous-immediate (NCI) software-force events: Such types of events are immediately effective on PWM outputs when triggered by software. The forcing is non-continuous, which means the next active timing events will be able to alter the PWM outputs.
*   Continuous (CNTU) software-force events: Such types of events are continuous. The forced PWM outputs will continue until they are released by software. The events' triggers are configurable. They can
```