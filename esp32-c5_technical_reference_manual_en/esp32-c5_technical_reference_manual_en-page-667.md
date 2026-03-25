

```markdown
2. Poll the reading of `SYSTIMER_TIMER_UNITn_VALUE_VALID` till it is 1. Then, user can read the count value from `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
3. Read the lower 32 bits and higher 20 bits from `SYSTIMER_TIMER_UNITn_VALUE_LO` and `SYSTIMER_TIMER_UNITn_VALUE_HI` respectively.

### 14.7.2 Configure a One-Time Alarm in Target Mode

1. Set `SYSTIMER_TARGETx_TIMER_UNIT_SEL` to select the counter (UNIT0 or UNIT1) used for comparison with COMPx.
2. Read the current count value with reference to Section 14.7.1. This value will be used to calculate the alarm value (t) in Step 4.
3. Clear `SYSTIMER_TARGETx_PERIOD_MODE` to enable target mode.
4. Set an alarm value (t), and fill its lower 32 bits into `SYSTIMER_TIMER_TARGETx_LO`, and the higher 20 bits into `SYSTIMER_TIMER_TARGETx_HI`.
5. Set `SYSTIMER_TIMER_COMPx_LOAD` to synchronize the alarm value (t) to COMPx, i.e., load the alarm value (t) to the COMPx.
6. Set `SYSTIMER_TARGETx_WORK_EN` to enable the selected COMPx. COMPx starts comparing the count value with the alarm value (t).
7. Set `SYSTIMER_TARGETx_INT_ENA` to enable the timer interrupt. When UNITn reaches the alarm value (t), a `SYSTIMER_TARGETx_INT` interrupt is triggered.

### 14.7.3 Configure Periodic Alarms in Period Mode

1. Set `SYSTIMER_TARGETx_TIMER_UNIT_SEL` to select the counter (UNIT0 or UNIT1) used for comparison with COMPx.
2. Set an alarm period ($\hat{t}$), and fill it into `SYSTIMER_TARGETx_PERIOD`.
3. Set `SYSTIMER_TIMER_COMPx_LOAD` to synchronize the alarm period ($\hat{t}$) to COMPx, i.e., load the alarm period ($\hat{t}$) to COMPx.
4. Clear and then set `SYSTIMER_TARGETx_PERIOD_MODE` to configure COMPx into period mode.
5. Set `SYSTIMER_TARGETx_WORK_EN` to enable the selected COMPx. COMPx starts comparing the count value with the sum of (start value + n×$\hat{t}$) ($n = 1, 2, 3...$).
6. Set `SYSTIMER_TARGETx_INT_ENA` to enable the timer interrupt. A `SYSTIMER_TARGETx_INT` interrupt is triggered when UNITn reaches start value + n×$\hat{t}$ ($n = 1, 2, 3...$) set in Step 2.

### 14.7.4 Update After Light-sleep

1. Configure RTC timer before the chip goes to Light-sleep mode, to record the exact sleep time. For more information, see Chapter 13 Low-Power Management.
2. Read the sleep time from the RTC timer when the chip wakes up from Light-sleep mode.
3. Read the current count value of system timer, see Section 14.7.1.
```