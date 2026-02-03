Title: Chapter 35 LED PWM Controller (LEDC)

Body Text:
To change the timer's clock divisor at runtime, first configure the `LEDC_CLK_DIV_TIMERx` field and then set the `LEDC_TIMERx_PARA_UP` field to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. `LEDC_TIMERx_PARA_UP` field will be automatically cleared by hardware.

Subtitle: 35.3.2.3 14-bit Counter

Body Text:
Each timer contains a 14-bit timebase counter that uses ref_pulsex as its reference clock (see Figure 35.3-1). The `LEDC_TIMERx_DUTY_RES` field configures the overflow value of this 14-bit counter. Hence, the maximum resolution of the PWM signal is 14 bits. The counter counts up to \(2^{LEDC_TIMERx_DUTY_RES} - 1\), overflows and begins counting from 0 again.

The counter can trigger `LEDC_TIMERx_OVF_INT` interrupt (generated automatically by hardware without configuration) every time the counter overflows. It can also be configured to trigger `LEDC_OVF_CNT_CHn_INT` interrupt after the counter overflows \(1\) times, plus configure

- LEDC_OVF_CNT_CHn
- LEDC_OVF_NUM_CHn

To configure:

1. Configure `LEDC_TIMERx_SEL_CHn` as the counter for the PWM generator.
2. Enable the counter by setting `LEDC_OVF_CNT_EN_CHn`.
3. Set `LEDC_OVF_NUM_CHn` to the number of counter overflows to generate an interrupt, minus 1
4. Enable the overflow interrupt by setting `LEDC_OVF_CNT_CHn_INT_ENA`
5. Set `LEDC_TIMERx_DUTY_RES` to enable the timer and wait for a `LEDC_OVF_CNT_CHn_INT` interrupt

Referring to Figure 35.3-1, the frequency of a PWM generator output signal (sig_out) is dependent on the frequency of the timer's clock source `LEDC_CLKx`, the clock divisor `LEDC_CLK_DIV`, and the duty resolution (counter width) `LEDC_TIMERx_DUTY_RES`.

Formula:
\[ f_{PWM} = \frac{f_{LEDClk}}{LEDClk_DIV \cdot 2^{LEDClk TIMERx DUTY RES}} \]

Based on this formula above, the desired duty resolution can be calculated as follows:

\[ LEDClk_TIMERx_DUTY_RES = log_2\left(\frac{f_{LEDClk}}{f_{PWM} \cdot LEDClk_DIV}\right) \]

Table 35.3-1 lists commonly-used frequencies and their corresponding resolutions.

Table: Table 35.3-1 Commonly-used Frequencies and Resolutions

| LEDC_CLKx | PWM Frequency       | Highest Resolution (bit) | Lowest Resolution (bit) |
|------------|----------------------|---------------------------|--------------------------|
|            |                      |                          |                         |
| APB_CLK   | 80 MHz              | 14                        | 7                        |
|            | 5 kHz               | 13                        | 4                        |
|            | 10 kHz             | 12                        | 3                        |
| XTAL_CLK  | (40 MHz)           | 14                        | 6                        |
| XTAL_CLK  | (40 MHz)           | 13                        | 4                        |

Footnotes:
1. The highest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is \(1\) and rounded down.
2. If the highest resolution calculated by the formula is higher than the counter's width, then the highest resolution should be \(14\) bits.

3. The lowest resolution is calculated when the clock divisor `LEDC_CLK_DIV` is 1023 + \(\frac{5}{2^{6}}\) and rounded up.
4. If the lowest resolution by formula calculation lower than \(0\), then the highest resolution should be \(1\).

Footer: ESP32-S3 TRM (Version 1.7)

Button: Submit Documentation Feedback