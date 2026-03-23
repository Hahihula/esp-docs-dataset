

```markdown
3. Get the timer’s current value.

* Write any value to `TIMG_TOUPDATE_REG` to latch the timer’s current value.
* Wait until `TIMG_TOUPDATE_REG` is cleared by hardware.
* Read the latched timer value from `TIMG_TOLO_REG` and `TIMG_TOHI_REG`.

### 14.4.2 Timer as One-shot Alarm

1. Configure the time-base counter following step 1 of Section 14.4.1.

2. Configure the alarm.

    * Configure the alarm value by setting `TIMG_TOALARMLO_REG` and `TIMG_TOALARMIHI_REG`.
    * Enable interrupt by setting `TIMG_TO_INT_ENA`.

3. Disable auto reload by clearing `TIMG_TO_AUTORELOAD`.

4. Start the alarm by setting `TIMG_TO_ALARM_EN`.

5. Handle the alarm interrupt.

    * Clear the interrupt by setting the timer’s corresponding bit in `TIMG_TO_INT_CLR`.
    * Disable the timer by clearing `TIMG_TO_EN`.

### 14.4.3 Timer as Periodic Alarm by APB

1. Configure the time-base counter following step 1 in Section 14.4.1.

2. Configure the alarm following step 2 in Section 14.4.2.

3. Enable auto reload by setting `TIMG_TO_AUTORELOAD` and configure the reload value via `TIMG_TO_LOAD_LO` and `TIMG_TO_LOAD_HI`.

4. Start the alarm by setting `TIMG_TO_ALARM_EN`.

5. Handle the alarm interrupt (repeat on each alarm iteration).

    * Clear the interrupt by setting the timer’s corresponding bit in `TIMG_TO_INT_CLR`.
    * If the next alarm requires a new alarm value and reload value (i.e. different alarm interval per iteration), then `TIMG_TOALARMLO_REG`, `TIMG_TOALARMIHI_REG`, `TIMG_TO_LOAD_LO`, and `TIMG_TO_LOAD_HI` should be reconfigured as needed. Otherwise, the aforementioned registers should remain unchanged.
    * Re-enable the alarm by setting `TIMG_TO_ALARM_EN`.

6. Stop the timer (on final alarm iteration).

    * Clear the interrupt by setting the timer’s corresponding bit in `TIMG_TO_INT_CLR`.
    * Disable the timer by clearing `TIMG_TO_EN`.
```