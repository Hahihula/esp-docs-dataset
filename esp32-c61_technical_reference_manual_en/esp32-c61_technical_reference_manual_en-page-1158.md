

```markdown
Chapter 31 LED PWM Controller (LEDC)                                                                 GoBack


LED_PWM
   Timer0 ──┬── Mux ──→ PWM0
   Timer1 ──┼──        │
   Timer2 ──┤           ├─→ PWM1
            │           │
            │           ├─→ PWM2
            │           │
            │           ├─→ PWM3
            │           │
            │           ├─→ PWM4
            │           │
            │           └─→ PWM5

Events ────────────────┐ Events and Tasks ────────────────→ Tasks
                        ↓
Figure 31.3-1. LED PWM Architecture


Each of the four timers has an internal timebase counter (i.e., a counter that counts on cycles of a reference clock) and thus can be independently configured (i.e., configurable clock divider, and counter overflow value). Each PWM generator selects one of the timers by configuring the `LEDC_TIMER_SEL_CHn`, and uses the timer’s counter value `timerx_cnt` as a reference to generate its PWM signal.

Figure 31.3-2 illustrates the main functional blocks of the timer and the PWM generator.


[Diagram: Timer and PWM Generator Block Diagram]

Timerx:
   ┌─────────────────────────────┐
   │ XTAL_40M_CLK                 │
   │ FOSC_20M_CLK                 │
   │ REF_80M_CLK                  │
   ├─────────────────────────────┤
   │ LEDC_CLK_DIV_TIMERx         │
   └──────────┬──────────────────┘
              │
              ▼
          Divider (18 bits)
              │
            ref_pulse_
              │
           Counter (20 bits)
              │
        LEDC_TIMERx_RST / LEDC_TIMERx_DUTY_RES
              │
         timerx_cnt ──┬──────────────┐
                     │                │
     LEDC_TIMERx_PAUSE ─┼────────────┤
                      ▼               ▼
   High/Low_level comparator ────────────────→ LEDC_SIG_OUT_EN_CHn

PWMn:
   ┌─────────────────────────────┐
   │ LEDC_DUTY_CHn                │
   │ LEDC_HPOINT_CHn              │
   ├─────────────────────────────┤
   │ Fading configurations' memory│
   └─────────────────────────────┘


Figure 31.3-2. Timer and PWM Generator Block Diagram


31.4 Functional Description

31.4.1 Timers

Each timer in LED PWM Controller internally maintains a timebase counter. Referring to Figure 31.3-2, this clock signal used by the timebase counter is named `ref_pulsex`. All timers use the same clock source `LEDC_CLK`, which is then passed through a clock divider to generate `ref_pulsex` for the counter.
```