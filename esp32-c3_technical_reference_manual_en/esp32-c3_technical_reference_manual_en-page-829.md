

```markdown
APB_CLK: Set LEDC_APB_CLK_SEL[1:0] to 1  
RC_FAST_CLK: Set LEDC_APB_CLK_SEL[1:0] to 2  
XTAL_CLK: Set LEDC_APB_CLK_SEL[1:0] to 3  

The LEDC_CLKx signal will then be passed through the clock divider.

## 32.3.2.2 Clock Divider Configuration

The LEDC_CLKx signal is passed through a clock divider to generate the ref_pulsex signal for the counter. The frequency of ref_pulsex is equal to the frequency of LEDC_CLKx divided by the divisor LEDC_CLK_DIV (see Figure 32.3-1).

The divisor LEDC_CLK_DIV is a fractional value. Thus, it can be a non-integer. LEDC_CLK_DIV is configured according to the following equation.

$$LEDC\_CLK\_DIV = A + \frac{B}{256}$$

*   `A` corresponds to the most significant 10 bits of `LEDC_CLK_DIV_TIMERx` (i.e. `LEDC_TIMERx_CONF_REG[21:12]`)
*   The fractional part `B` corresponds to the least significant 8 bits of `LEDC_CLK_DIV_TIMERx` (i.e. `LEDC_TIMERx_CONF_REG[11:4]`)

When the fractional part `B` is zero, LEDC_CLK_DIV is equivalent to an integer divisor (i.e. an integer prescaler). In other words, a ref_pulsex clock pulse is generated after every A number of LEDC_CLKx clock pulses.

However, when B is nonzero, LEDC_CLK_DIV becomes a non-integer divisor. The clock divider implements non-integer frequency division by alternating between `A` and `(A+1)` LEDC_CLKx clock pulses per ref_pulsex clock pulse. This will result in the average frequency of ref_pulsex clock pulse being the desired frequency (i.e. the non-integer divided frequency). For every 256 ref_pulsex clock pulses:

*   A number of `B` ref_pulsex clock pulses will consist of `(A+1)` LEDC_CLKx clock pulses
*   A number of `(256-B)` ref_pulsex clock pulses will consist of a LEDC_CLKx clock pulses
*   The ref_pulsex clock pulses consisting of `(A+1)` pulses are evenly distributed amongst those consisting of `A` pulses

Figure 32.3-2 illustrates the relation between LEDC_CLKx clock pulses and ref_pulsex clock pulses when dividing by a non-integer LEDC_CLK_DIV.

![Frequency Division When LEDC_CLK_DIV is a Non-Integer Value](#)
```