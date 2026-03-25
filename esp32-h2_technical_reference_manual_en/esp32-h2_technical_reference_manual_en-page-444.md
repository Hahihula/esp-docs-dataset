

```markdown
Chapter 12 System Timer (SYSTIMER)

3. Read the lower 32 bits and higher 20 bits from SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI respectively.

12.5.2 Configure a One-Time Alarm in Target Mode

1. Set SYSTIMER_TARGETx_TIMER_UNIT_SEL to select the counter (UNIT0 or UNIT1) used for comparison with COMPx.
2. Read the current count value, see Section 12.5.1. This value will be used to calculate the alarm value (t) in Step 4.
3. Clear SYSTIMER_TARGETx_PERIOD_MODE to enable target mode.
4. Set an alarm value (t), and fill its lower 32 bits into SYSTIMER_TIMER_TARGETx_LO, and the higher 20 bits into SYSTIMER_TIMER_TARGETx_HI.
5. Set SYSTIMER_TIMER_COMPx_LOAD to synchronize the alarm value (t) to COMPx, i.e., load the alarm value (t) to the COMPx.
6. Set SYSTIMER_TARGETx_WORK_EN to enable the selected COMPx. COMPx starts comparing the count value with the alarm value (t).
7. Set SYSTIMER_TARGETx_INT_ENA to enable the timer interrupt. When Unitn reaches the alarm value (t), a SYSTIMER_TARGETx_INT interrupt is triggered.

12.5.3 Configure Periodic Alarms in Period Mode

1. Set SYSTIMER_TARGETx_TIMER_UNIT_SEL to select the counter (UNIT0 or UNIT1) used for comparison with COMPx.
2. Set an alarm period (δt), and fill it into SYSTIMER_TARGETx_PERIOD.
3. Set SYSTIMER_TIMER_COMPx_LOAD to synchronize the alarm period (δt) to COMPx, i.e., load the alarm period (δt) to COMPx.
4. Clear and then set SYSTIMER_TARGETx_PERIOD_MODE to configure COMPx into period mode.
5. Set SYSTIMER_TARGETx_WORK_EN to enable the selected COMPx. COMPx starts comparing the count value with the sum of (start value + n×δt) (n = 1, 2, 3...).
6. Set SYSTIMER_TARGETx_INT_ENA to enable the timer interrupt. A SYSTIMER_TARGETx_INT interrupt is triggered when Unitn reaches start value + n×δt (n = 1, 2, 3...) set in Step 2.

12.5.4 Update After Light-sleep

1. Configure RTC timer before the chip goes into Light-sleep mode, to record the exact sleep time. For more information, see Chapter 11 Low-Power Management.
2. Read the sleep time from the RTC timer when the chip wakes up from Light-sleep mode.
3. Read the current count value of system timer, see Section 12.5.1.
4. Convert the time value recorded by the RTC timer from the clock cycles based on RTC_SLOW_CLK to that based on 16 MHz CNT_CLK. For example, if the frequency of RTC_SLOW_CLK is 32 kHz, the recorded RTC timer value should be converted by multiplying by 500.
```