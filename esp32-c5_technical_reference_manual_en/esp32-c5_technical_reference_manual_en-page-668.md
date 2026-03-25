

```markdown
Chapter 14 System Timer

GoBack

4. Convert the time value recorded by RTC timer from the clock cycles based on RTC_SLOW_CLK to that based on 16 MHz CNT_CLK. For example, if the frequency of RTC_SLOW_CLK is 32 kHz, the recorded RTC timer value should be converted by multiplying by 500.

5. Add the converted RTC value to the current count value of system timer:

- Fill the new value into SYSTIMER_TIMER_UNITn_LOAD_LO (low 32 bits) and SYSTIMER_TIMER_UNITn_LOAD_HI (high 20 bits).

- Set SYSTIMER_TIMER_UNITn_LOAD to load the new timer value into the system timer. By such way, the system timer is updated.
```