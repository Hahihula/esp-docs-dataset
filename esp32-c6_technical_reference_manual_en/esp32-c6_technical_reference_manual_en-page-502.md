

```markdown
2. Read current count value, see Section 13.5.1. This value will be used to calculate the alarm value (t) in Step 4.
3. Clear SYSTIMER_TARGETx_PERIOD_MODE to enable target mode.
4. Set an alarm value (t), and fill its lower 32 bits to SYSTIMER_TIMER_TARGETx_LO, and the higher 20 bits to SYSTIMER_TIMER_TARGETx_HI.
5. Set SYSTIMER_TIMER_COMPx_LOAD to synchronize the alarm value (t) to COMPx, i.e., load the alarm value (t) to the COMPx.
6. Set SYSTIMER_TARGETx_WORK_EN to enable the selected COMPx. COMPx starts comparing the count value with the alarm value (t).
7. Set SYSTIMER_TARGETx_INT_ENA to enable timer interrupt. When Unitn counts to the alarm value (t), a SYSTIMER_TARGETx_INT interrupt is triggered.

13.5.3 Configure Periodic Alarms in Period Mode

1. Set SYSTIMER_TARGETx_TIMER_UNIT_SEL to select the counter (UNIT0 or UNIT1) used for COMPx.
2. Set an alarm period (δt), and fill it to SYSTIMER_TARGETx_PERIOD.
3. Set SYSTIMER_TIMER_COMPx_LOAD to synchronize the alarm period (δt) to COMPx, i.e., load the alarm period (δt) to COMPx.
4. Clear and then set SYSTIMER_TARGETx_PERIOD_MODE to configure COMPx into period mode.
5. Set SYSTIMER_TARGETx_WORK_EN to enable the selected COMPx. COMPx starts comparing the count value with the sum of (start value + n*δt) (n = 1, 2, 3...).
6. Set SYSTIMER_TARGETx_INT_ENA to enable timer interrupt. A SYSTIMER_TARGETx_INT interrupt is triggered when Unitn counts to start value + n*δt (n = 1, 2, 3...) set in Step 2.

13.5.4 Update After Light-sleep

1. Configure the RTC timer before the chip goes to Light-sleep mode, to record the exact sleep time. For more information, see Chapter 12 Low-Power Management.
2. Read the sleep time from the RTC timer when the chip is woken up from Light-sleep mode.
3. Read current count value of system timer, see Section 13.5.1.
4. Convert the time value recorded by the RTC timer from the clock cycles based on RTC_SLOW_CLK to that based on 16 MHz CNT_CLK. For example, if the frequency of RTC_SLOW_CLK is 32 kHz, the recorded RTC timer value should be converted by multiplying by 500.
5. Add the converted RTC value to the current count value of the system timer:
    * Fill the new value into SYSTIMER_TIMER_UNITn_LOAD_LO (low 32 bits) and SYSTIMER_TIMER_UNITn_LOAD_HI (high 20 bits).
    * Set SYSTIMER_TIMER_UNITn_LOAD to load new timer value into system timer. By such way, the system timer is updated.
```