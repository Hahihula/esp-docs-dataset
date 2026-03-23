

```markdown
LED_PWM
Timer0 → Mux → PWM0
Timer1 → Mux → PWM1
Timer2 → Mux → PWM2
Timer3 → Mux → PWM3, PWM4, PWM5

Tasks → Events and Tasks → Events

Figure 35.2-1. LED PWM Architecture


# 35.3 Functional Description

## 35.3.1 Architecture

Figure 35.2-1 shows the architecture of the LED PWM Controller.

Each of the four timers has an internal timebase counter (i.e. a counter that counts on cycles of a reference clock) and thus can be independently configured (i.e. configurable clock divider, and counter overflow value).

Each PWM generator selects one of the timers by configuring the `LEDC_TIMER_SEL_CHn`, and uses the timer’s counter value `timerx_cnt` as a reference to generate its PWM signal.

Figure 35.3-1 illustrates the main functional blocks of the timer and the PWM generator.


PLL_F80M_CLK
RC_FAST_CLK
XTAL_CLK

Timerx
LEDC_CLK_DIV_TIMERx → Divider (18 bits) → Counter (20 bits)
LEDC_CLKx, LEDC_TIMERx, PAUSE → ref_pulsei → timerx_cnt

PWMn
LEDC_DUTY_CHn → LEDC_HIPOT_CHn → High/Low level comparator → Fading ranges memory
LEDC_SIG_OUT_EN_CHn → sig_out

Figure 35.3-1. Timer and PWM Generator Block Diagram
```