**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Table Header:**
Table 35.3-1. Commonly-used Frequencies and Resolutions

| LEDEC_CLKx | RC_FAST_CLK (17.5 MHz) | RC_FAST_CLK (17.5 MHz) |
|-------------|-------------------------|-------------------------|
|             | Highest Resolution (bit)| Lowest Resolution (bit) |
| 1           |                         | 1                       |
|             |                         | 4                       |

**Body Text:**

The highest resolution is calculated when the clock divisor LEDEC_CLK_DIV is 1 and rounded down. If the highest resolution calculated by the formula is higher than the counter’s width 14 bits, then the highest resolution should be 14 bits.

The lowest resolution is calculated when the clock divisor LEDEC_CLK_DIV is \(1023 + \frac{5}{256}\) and rounded up. If the lowest resolution calculated by the formula is lower than O, then the lowest resolution should be 1.

To change the overflow value at runtime, first set the LEDEC_TIMERx_DUTY_RES field, and then set the LEDEC_TIMERx_PARA_UP field. This will cause the newly configured values to take effect upon the next overflow of the counter. If LEDEC_OVF_CNT_EN_CHn is reconfigured, LEDC PARA UP CHn should be set to apply the new configuration.

In summary, these configuration values need to be updated by setting LEDEC_TIMERx_PARA_UP or LEDC PARA UP CHn in LEDEC_TIMERx_PARA_UP and LEDC PARA UP CHn will be automatically cleared by hardware.

**Subsection Title:**
35.3.3 PWM Generators

To generate a PWM signal, a PWM generator (PWMn) selects a timer (Timerx). Each PWM generator can be configured separately by setting LEDC_TIMER_SEL_CHn to use one of four timers to generate the PWM output.
As shown in Figure 35.3-1, each PWM generator has a comparator and two multiplexers. A PWM generator compares the timer’s 14-bit counter value (Timerx_cnt) to two trigger values Hpointn and Lpointn. When the timer's counter value is equal to Hpointn or Lpointn, the PWM signal is high or low, respectively.

Below are conditions for generating a fixed duty cycle:
- If Timerx_cnt == Hpointn, sig_outn = 1.
- If Timerx_cnt == Lpointn, sig_outn = 0. 

**Figure Description:**
Figure 35.3-3 illustrates how Hpointn or Lpointn are used to generate a fixed duty cycle PWM output signal.

**Footer Information:**
Espressif Systems
Page number: 1314
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback