

```markdown
Chapter 13 XTAL32K Watchdog Timers (XTWDT)
GoBack

- Calculate the sum of divisor components S according to the frequency of RC_SLOW_CLK and the desired frequency of BACKUP32K_CLK;
- Calculate the integer part of divisor N = f_rc_slow_clk / f_back_clk;
- Calculate the integer part of divisor component M = N/2. The integer part of divisor N are separated into two parts because a divisor component corresponds to a pulse width in high or low state;
- Calculate the number of divisor components that equal M (x_n = M) and the number of divisor components that equal M + 1 (x_n = M + 1) according to the value of M and S. (M + 1) is the fractional part of divisor component.

For example, if the frequency of RC_SLOW_CLK is 163 kHz, then f_rc_slow_clk = 163000,
f_back_clk = 32768, S = 20, M = 2, and {x₀,x₁,x₂,x₃,x₄,x₅,x₆,x₇} = {2,3,2,3,2,3,2,3}. As a result, the frequency of BACKUP32K_CLK is 32.6 kHz.
```