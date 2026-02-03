**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Menu Options:**
- APB_CLK: Set LEDC_APB_CLK_SEL[1:0] to 1
- RC_FAST_CLK: Set LEDC_APB_CLK_SEL[1:0] to 2
- XTAL_CLK: Set LEDC_APB_CLK_SEL[1:0] to 3

**Section Title and Subtitle:**
35.3.2.2 Clock Divider Configuration

**Body Text:**
The LEDC_CLKx signal is passed through a clock divider to generate the ref_pulsex signal for the counter. The frequency of ref_pulselx is equal to the frequency of LEDC_CLKx divided by the divisor LEDC_CLK_DIV (see Figure 35.3-1).

The divisor LEDC_CLK_DIV is a fractional value. Thus, it can be a non-integer divisor. LEDC_CLK_DIV is configured according to the following equation:

\[ \text{LEDC_CLK_DIV} = A + \frac{B}{2^M} \]

- \(A\) corresponds to the most significant 10 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[21:12]`)
- The fractional part \( B \) corresponds to the least significant 8 bits of `LEDC_CLK_DIV_TIMERx` (i.e., `LEDC_TIMERx_CONF_REG[11:4]`)

When the fractional part \(B\) is zero, LEDC_CLK_DIV is equivalent to an integer divisor. In other words, a ref_pulselx clock pulse is generated after every A number of LEDC_CLKx clock pulses.

However, when B is nonzero, `LEDC_CLK_DIV` becomes a non-integer divisor. The clock divider implements non-integer frequency division by alternating between \(A\) and \((A+1)\) `LEDC_CLKx` clock pulses per ref_pulselx clock pulse. This will result in the average frequency of ref_pulselx clock pulses being the desired frequency (i.e., the non-integer divided frequency). For every 256 ref_pulselx clock pulses:

- A number of \(B\) `ref_pulsex` clock pulses will consist of \((A+1)\) `LEDC_CLKx` clock pulses
- A number of \((256-B)\) `ref_pulsex` clock pulses will consist of a `LEDC_CLKx` clock pulse

The ref_pulselx clock pulses consisting of \( (A+1) \) pulses are evenly distributed amongst those consisting of \(A\) pulses.

**Figure Description:**
Figure 35.3-2 illustrates the relation between LEDC_CLKx clock pulses and ref_pulselx clock pulses when dividing by a non-integer LEDC_CLK_DIV.
(Figure shows an illustration with labels indicating A clock pulses, B (A+1) counts)

**Footer Information:**
Espressif Systems
Page number 1312
Document version ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback