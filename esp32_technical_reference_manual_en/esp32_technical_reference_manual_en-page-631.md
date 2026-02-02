**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Equation:**
\[ f_{\text{sig\_out}} = \frac{\int_{\text{LEDCL\_CLKx}}}{\text{LEDCL\_DIVX} \cdot \text{LEDC\_HSTIMERx\_DUTY\_RES}} \]

**Body Text Explanation of Equation:**
Based on the formula above, the desired duty resolution can be calculated as follows:

\[ \text{LEDC\_HSTIMERx\_DUTY\_RES} = \log_2\left(\frac{\int_{\text{LEDCL\_CLKx}}}{f_{\text{sig\_out}} \cdot \text{LEDC\_CLKx\_DIVX}}\right) \]

**Table Title:**
Table 28.2-1 Commonly-used Frequencies and Resolutions

| LEDC_CLKx | PWM Frequency       | Highest Resolution (bit) | Lowest Resolution (bit) |
|------------|----------------------|---------------------------|-------------------------|
|            |                      |                          |                         |
| APB_CLK   | 80 MHz               | 16                        | 7                       |
|            |                      |                           |                         |
| APB_CLK   | 5 kHz                | 13                        | 4                       |
|            |                      |                           |                         |
| APB_CLK   | 80 MHz               | 12                        | 3                       |
| RC_FAST_CLK| 8 MHz                | 12                        | 3                       |
| RC_FAST_CLK| 2 kHz                | 11                        | 2                       |
| REF_TICK   | 1 MHz                | 9                         | 1                       |

**Table Notes:**
1. The highest resolution is calculated when the clock divisor LEDC_CLKxDIVx is set to '1' and rounded down.
2. If the lowest resolution calculation by formula is lower than zero, then the lowest resolution should be one.

**Additional Text Explanation of Table:**

The low-speed timers I_timerx on the low-speed channel differ from high-speed timers h_timerr in two aspects:

1. Where the high-speed timer clock source can be clocked from REF_TICK or APB_CLK, and where these are sourced either from REF_TICK or SLOW_CLOCK.
2. The high-speed counter and divider values will update after next overflow interrupt.

**Subsection Title:**
28.2.3 Channels

**Body Text for Subsection 28.2.3:**

A channel takes the two-bit value of a selected timer's counter to set its output, which is compared with LEDC_HPOINT_HSCHn; if these match, then latch high.
LEDC_HPOINT_HSChn and LEDC_DUTY_HSChn [24..4]. When this matches, it latches low.

**Footer:**
Espressif Systems
631 ESP32 TRM (Version 5.6)
Submit Documentation Feedback