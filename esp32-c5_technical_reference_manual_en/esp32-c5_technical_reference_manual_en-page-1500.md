

```markdown
Chapter 40 LED PWM Controller (LEDC)

GoBack

40.4.1.1 Clock Source

LED PWM registers configured by software are clocked by APB_CLK. To use the LED PWM peripheral, the APB_CLK signal going to the LED PWM has to be enabled. The APB_CLK signal to LED PWM can be enabled by setting the `PCR_LEDC_CLK_EN` field in the `PCR_LEDC_CONF_REG` register. The LEDC_CLK signal to LED PWM can be enabled by setting the `PCR_LEDC_SCLK_EN` field in the `PCR_LEDC_SCLK_CONF_REG` register. The LED PWM peripheral can be reset via software by setting the `PCR_LEDC_RST_EN` field in the `PCR_LEDC_CONF_REG` register.

Timers in the LED PWM Controller choose their common clock source from one of the following clock signals: XTAL_CLK, RC_FAST_CLK, and PLL_F80M_CLK. The procedure for selecting a clock source signal for LEDC_CLK is described below:

*   `XTAL_CLK`: Set `PCR_LEDC_SCLK_SEL[1:0]` to 0
*   `RC_FAST_CLK`: Set `PCR_LEDC_SCLK_SEL[1:0]` to 1
*   `PLL_F80M_CLK`: Set `PCR_LEDC_SCLK_SEL[1:0]` to 2

The LEDC_CLK signal will then be passed through the clock divider.

For more information, please refer to Chapter 9 Reset and Clock.

40.4.1.2 Clock Divider Configuration

The LEDC_CLK signal is passed through a clock divider to generate the `ref_pulsex` signal for the counter. The frequency of `ref_pulsex` is equal to the frequency of LEDC_CLK divided by the divisor LEDC_CLK_DIV (see Figure 40.3-2).

The clock divider is a fractional divider. Thus, the divisor `LEDC_CLK_DIV` can be non-integer values. `LEDC_CLK_DIV` is configured according to the following equation.

```latex
LEDC_CLK_DIV = A + \frac{B}{256}
\quad (40.1)
```

*   The integer part `A` corresponds to the most significant 10 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[22:13]`)
*   The fractional part `B` corresponds to the least significant 8 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[12:5]`)

When the fractional part `B` is 0, LEDC_CLK_DIV is equivalent to an integer divisor (i.e., an integer prescaler). In other words, a `ref_pulsex` clock pulse is generated after every `A` number of LEDC_CLK clock pulses.

However, when `B` is not 0, LEDC_CLK_DIV becomes a non-integer divisor. The clock divider implements non-integer frequency division by alternating between `A` and `(A+1)` LEDC_CLK clock pulses per `ref_pulsex` clock pulse. In this way, the average frequency of `ref_pulsex` clock pulse will be the desired frequency (i.e., the non-integer divided frequency). For every 256 `ref_pulsex` clock pulses:

*   A number of `B` `ref_pulsex` clock pulses are generated every `(A+1)` LEDC_CLK clock pulses
*   A number of `(256-B)` `ref_pulsex` clock pulses are generated every `A` LEDC_CLK clock pulses
*   The `ref_pulsex` clock pulses generated every `(A+1)` pulses are evenly distributed amongst those generated every `A` pulses

```markdown
Espressif Systems
1500
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```