

```markdown
3. Get the timer’s current value.

- Write any value to `TIMGn_TOUPDATE_REG` to latch the timer’s current value.
- Wait until `TIMGn_TOUPDATE_REG` is cleared by hardware.
- Read the latched timer value from `TIMGn_TOLO_REG` and `TIMGn_TOHI_REG`.

### 13.4.2 Timer as One-shot Alarm

1. Configure the time-base counter following step 1 of Section 13.4.1.

2. Configure the alarm.
    - Configure the alarm value by setting `TIMGn_TOALARMLO_REG` and `TIMGn_TOALARMIHI_REG`.
    - Enable interrupt by setting `TIMGn_TO_INT_ENA`.

3. Disable auto reload by clearing `TIMGn_TO_AUTORELOAD`.

4. Start the alarm by setting `TIMGn_TO_ALARM_EN`.

5. Handle the alarm interrupt.
    - Clear the interrupt by setting the timer’s corresponding bit in `TIMGn_TO_INT_CLR`.
    - Disable the timer by clearing `TIMGn_TO_EN`.

### 13.4.3 Timer as Periodic Alarm by APB

1. Configure the time-base counter following step 1 in Section 13.4.1.

2. Configure the alarm following step 2 in Section 13.4.2.

3. Enable auto reload by setting `TIMGn_TO_AUTORELOAD` and configure the reload value via `TIMGn_TO_LOAD_LO` and `TIMGn_TO_LOAD_HI`.

4. Start the alarm by setting `TIMGn_TO_ALARM_EN`.

5. Handle the alarm interrupt (repeat on each alarm iteration).
    - Clear the interrupt by setting the timer’s corresponding bit in `TIMGn_TO_INT_CLR`.
    - If the next alarm requires a new alarm value and reload value (i.e., different alarm interval per iteration), then `TIMGn_TOALARMLLO_REG`, `TIMGn_TOALARMIHI_REG`, `TIMGn_TO_LOAD_LO`, and `TIMGn_TO_LOAD_HI` should be reconfigured as needed. Otherwise, the aforementioned registers should remain unchanged.
    - Re-enable the alarm by setting `TIMGn_TO_ALARM_EN`.

6. Stop the timer (on final alarm iteration).
    - Clear the interrupt by setting the timer’s corresponding bit in `TIMGn_TO_INT_CLR`.
    - Disable the timer by clearing `TIMGn_TO_EN`.
```