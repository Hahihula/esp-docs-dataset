

```markdown
LED_PWM
Timer0   ────► Mux ────► PWM0
Timer1   ────►         │
Timer2   ────►         │
Timer3   ────►         │
                      │
Events and Tasks      ► Events and Tasks
                      │
Tasks                 ► Tasks

Figure 40.3-1. LED PWM Architecture

Each of the four timers has an internal timebase counter (i.e., a counter that counts on cycles of a reference clock) and thus can be independently configured (i.e., configurable clock divider, and counter overflow value). Each PWM generator selects one of the timers by configuring the `LEDC_TIMER_SEL_CHn`, and uses the timer’s counter value `timerx_cnt` as a reference to generate its PWM signal.

Figure 40.3-2 illustrates the main functional blocks of the timer and the PWM generator.

[Block Diagram: Timer and PWM Generator Block Diagram]

Figure 40.3-2. Timer and PWM Generator Block Diagram

40.4 Functional Description

40.4.1 Timers

Each timer in LED PWM Controller internally maintains a timebase counter. Referring to Figure 40.3-2, this clock signal used by the timebase counter is named `ref_pulsex`. All timers use the same clock source LEDC_CLK, which is then passed through a clock divider to generate `ref_pulsex` for the counter.
```