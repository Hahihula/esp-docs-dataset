

```markdown
35.3.2 Timers

Each timer in LED PWM Controller internally maintains a timebase counter. Referring to Figure 35.3-1, this clock signal used by the timebase counter is named ref_pulsex. All timers use the same clock source LEDC_CLKx, which is then passed through a clock divider to generate ref_pulsex for the counter.

35.3.2.1 Clock Source

LED PWM registers configured by software are clocked by APB_CLK. To use the LED PWM peripheral, the APB_CLK signal going to the LED PWM has to be enabled. The APB_CLK signal to LED PWM can be enabled by setting the `PCR_LEDC_CLK_EN` field in the `PCR_LEDC_CONF_REG` register, and reset via software by setting the `PCR_LEDC_RST_EN` field in the `PCR_LEDC_CONF_REG` register.

Timers in LED PWM Controller choose their common clock source from one of the following clock signals: PLL_F96M_CLK, RC_FAST_CLK, and XTAL_CLK. The procedure for selecting a clock source signal for LEDC_CLKx is described below:

*   PLL_F96M_CLK: Set `LEDC_SCLK_SEL[1:0]` to 1
*   RC_FAST_CLK: Set `LEDC_SCLK_SEL[1:0]` to 2
*   XTAL_CLK: Set `LEDC_SCLK_SEL[1:0]` to 3

The LEDC_CLKx signal will then be passed through the clock divider.

If `LEDC_SCLK_SEL[1:0]` is set to 0 (an invalid value), LED PWM Controller cannot perform any function due to no clock source.

For more information, please refer to Chapter 7 Reset and Clock.

35.3.2.2 Clock Divider Configuration

The LEDC_CLKx signal is passed through a clock divider to generate the ref_pulsex signal for the counter. The frequency of ref_pulsex is equal to the frequency of LEDC_CLKx divided by the divisor LEDC_CLK_DIV (see Figure 35.3-1).

The divisor `LEDC_CLK_DIV` can be non-integer values, and it is configured according to the following equation.

```markdown
LEDC_CLK_DIV = A + B/256

*   The integer part A corresponds to the most significant 10 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[22:13]`)
*   The fractional part B corresponds to the least significant 8 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[12:5]`)
```

When the fractional part B is 0, LEDC_CLK_DIV is an integer (i.e., an integer prescaler). In other words, a ref_pulsex clock pulse is generated after every A LEDC_CLKx clock pulses.

However, when B is not 0, LEDC_CLK_DIV becomes a non-integer. The clock divider implements non-integer frequency division by generating a ref_pulsex clock pulse after every A and (A+1) LEDC_CLKx clock pulses alternately. In this way, the average frequency of ref_pulsex clock pulse will be the desired frequency (i.e., the non-integer divided frequency). For every 256 ref_pulsex clock pulses:

*   A number of B ref_pulsex clock pulses are generated every (A+1) LEDC_CLKx clock pulses
```