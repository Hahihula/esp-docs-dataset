

```markdown
Chapter 55 LED PWM Controller (LEDC)                                                                 GoBack


LED_PWM
├── Timer0 → Mux → PWM0
├── Timer1 → Mux → PWM1
├── Timer2 → Mux → PWM2
├── Timer3 → Mux → PWM3
│        │       │       │
│        └───────► PWM4
│                │       │
│                └───────► PWM5
└───────────────────────► PWM6
                          │
                          └───────► PWM7

Events ↔ Events and Tasks ↔ Tasks


Each of the four timers has an internal timebase counter (i.e., a counter that counts on cycles of a reference clock) and thus can be independently configured (i.e., configurable clock divider, and counter overflow value). Each PWM generator selects one of the timers by configuring the LEDC_TIMER_SEL_CHn, and uses the timer’s counter value timerx_cnt as a reference to generate its PWM signal.

Figure 55.3-2 illustrates the main functional blocks of the timer and the PWM generator.


Timerx
│
├── Input: XTAL_40M_CLK / FOSC_20M_CLK / REF_80M_CLK (via LEDC_SCLK_SEL[1:0])
│
└── Divider (18 bits) → ref_pulse
                         │
                         └── Counter (20 bits)
                               │
                               └── timerx_cnt
                                     │
                                     └── LEDC_TIMER_SEL_CHn → PWM generator input

PWMn
│
├── Input: timerx_cnt from Timerx via LEDC_TIMER_SEL_CHn
│
└── High/Low_level comparator (with Fading configurations' memory)
       │
       └── Output: sig_out, controlled by LEDC_IDLE_LV_CHn and other config registers


Figure 55.3-2. Timer and PWM Generator Block Diagram


55.4 Functional Description

55.4.1 Timers

Each timer in LED PWM Controller internally maintains a timebase counter. Referring to Figure 55.3-2, this clock signal used by the timebase counter is named ref_pulsex. All timers use the same clock source LEDC_CLK, which is then passed through a clock divider to generate ref_pulsex for the counter.


Espressif Systems      2775
Submit Documentation Feedback       ESP32-P4 TRM PRELIMINARY
```