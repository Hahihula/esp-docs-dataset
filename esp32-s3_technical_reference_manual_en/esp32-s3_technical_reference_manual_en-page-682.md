**Chapter Title:**
Chapter 14 XTAL32K Watchdog Timers (XTWDT)

**Body Text:**

- Calculate the sum of divisor components S according to the frequency of RC_SLOW_CLK and the desired frequency of BACKUP32K_CLK;
  
- Calculate the integer part of divisor N = f_rc_slow_clk / f_back_clk;

- Calculate the integer part of divisor component M = N/2. The integer part of divisor N are separated into two parts because a divisor component corresponds to a pulse width in high or low state;

- Calculate the number of divisor components that equal M (xn = M) and the number of divisor components that equal M + 1 (xn = M + 1) according to the value of M and S. (M + 1) is the fractional part of divisor component.

**Example:**
For example, if the frequency of RC_SLOW_CLK is 163 kHz, then f_rc_slow_clk = 163000,
f_back_clk = 32768, S = 20, M = 2, and {x0, x1, x2, x3, x4, x5, x6, x7} = {2, 3, 2, 3, 2, 3}. As a result, the frequency of BACKUP32K_CLK is 32.6 kHz.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)