**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Section Heading: Software-Force Events**

**Body Text:**
There are two types of software-force events inside the PWM generator:

1. **Non-continuous-immediate (NCI) software-force events**: Such types of events are immediately effective on PWM outputs when triggered by software. The forcing is non-continuous, meaning the next active timing events will be able to alter the PWM outputs.

2. **Continuous (CNTU) software-re-force events**: Such types of events are continuous. The forced PWM outputs will continue until they are released by software. The events' triggers are configurable. They can be timing events or immediate events.

**Figure Caption:**
Figure 36.3-19 shows a waveform of NCI software-force events. NCI events are used to force PWMxA output low. Forcing on PWMxB is disabled in this case.
*Note:* Period = 6, A = 3

**Diagram Description (partially transcribed):**
The diagram illustrates the timing and relationship between different signals such as PWM timer, UTEP, UTEZ, UTEA, NCI force event, PWMxA, and PWMxB. The waveform shows how these events interact over time.

**Footer:**
Espressif Systems
1348 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback