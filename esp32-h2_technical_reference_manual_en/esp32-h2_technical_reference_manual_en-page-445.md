

```markdown
Chapter 12 System Timer (SYSTIMER)    GoBack


5. Add the converted RTC value to the current count value of system timer:

- Fill the new value into SYSTIMER_TIMER_UNITn_LOAD_LO (low 32 bits) and SYSTIMER_TIMER_UNITn_LOAD_HI (high 20 bits).

- Set SYSTIMER_TIMER_UNITn_LOAD to load the new timer value into the system timer. By such way, the system timer is updated.
```