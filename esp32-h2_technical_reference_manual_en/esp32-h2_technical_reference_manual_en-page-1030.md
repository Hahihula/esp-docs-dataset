

```markdown
LED_PWM
Timer0 → Mux → PWM0
Timer1 → Mux → PWM1
Timer2 → Mux → PWM2
Timer3 → Mux → PWM3
                      ↓
Tasks → Events and Tasks → Events
```

Figure 35.2-1. LED PWM Architecture

## 35.3 Functional Description

### 35.3.1 Architecture

Figure 35.2-1 shows the architecture of the LED PWM Controller.

Each of the four timers has an internal timebase counter (i.e., a counter that counts on cycles of a reference clock) and thus can be independently configured (i.e., configurable clock divider, and counter overflow value). Each PWM generator selects one of the timers by configuring `LEDC_TIMER_SEL_CHn`, and uses the timer’s counter value `timerx_cnt` as a reference to generate its PWM signal.

Figure 35.3-1 illustrates the main functional blocks of the timer and the PWM generator.
```markdown
LEDC_SCLK_SEL[1:0]
PLL_F96M_CLK
RC_FAST_CLK
XTAL_CLK

Timerx → LEDC_TIMER_DIV_TIMERx → Divider (18 bits) ref_pulsex → Counter (20 bits)
        ↓
        LEDC_CLKx

LEDC_TIMER_SEL_CHn → PWMn
                    ↓
High/Low_level comparator
Fading configurations memory
LEDC_DUTY_START_Chn, LEDC_GAMMA_PAUSE, etc.

LEDC_DUTY_HPOINT_Ch1 → 0/1 → sig_outn
LEDC_SIG_OUT_EN_Chn

timerx_cnt
timerx_cnt
timerx_cnt
```

Figure 35.3-1. Timer and PWM Generator Block Diagram
```