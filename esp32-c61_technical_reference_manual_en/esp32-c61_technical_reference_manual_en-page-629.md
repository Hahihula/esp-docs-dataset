

```markdown
- If `TIMG_TO_AUTORELOAD` is 0, the current counter value is overwritten by the reloaded value because of the TGO_TASK_CNT_RELOAD_TIMERO and TG1_TASK_CNT_RELOAD_TIMERO. The alarm generation will be reopened by TGO_TASK_ALARM_START_TIMERO and TG1_TASK_ALARM_START_TIMERO.

9. Stop the timer (on final alarm iteration).
  - Disable the ETM channels used to map timer group's event and task
  - Set `TIMER_ETM_EN` to 0.
  - Clear the interrupt by setting the timer's corresponding bit in `TIMG_TO_INT_CLR`.
  - Disable the timer by clearing `TIMG_TO_EN`.

## 13.7.5 Frequency Calculation of Slow Clock

### 1. One-shot frequency calculation
- Select the clock whose frequency is to be calculated via `PCR_32_SEL`. For the relationship between the value of this register and the clock source, please refer to Chapter 15 RTC Timer.
- To meet the prerequisites for calculating the slow clock frequency, prescale RC_FAST_CLK via `PCR_FOSC_TICK_NUM`.
- Configure the time of calculation via `TIMG_RTC_CALI_MAX`.
- Select one-shot frequency calculation by clearing `TIMG_RTC_CALI_START_CYCLING`, and enable the two counters via `TIMG_RTC_CALI_START`.
- Once `TIMG_RTC_CALI_RDY` becomes 1, read `TIMG_RTC_CALI_VALUE` to get the value of XTAL_CLK's counter, and calculate the frequency of slow clock according to the formula in Section 13.4.5.

### 2. Periodic frequency calculation
- Select the clock whose frequency is to be calculated via `PCR_32_SEL`.
- To meet the prerequisites for calculating the slow clock frequency, prescale RC_FAST_CLK via `PCR_FOSC_TICK_NUM`.
- Configure the time of calculation via `TIMG_RTC_CALI_MAX`.
- Select periodic frequency calculation by enabling `TIMG_RTC_CALI_START_CYCLING`.
- When `TIMG_RTC_CALI_CYCLING_DATA_VLD` is 1, `TIMG_RTC_CALI_VALUE` is valid.

### 3. Timeout
If the counter of slow clock cannot finish counting in `TIMG_RTC_CALI_TIMEOUT_RST_CNT` cycles, `TIMG_RTC_CALI_TIMEOUT` will be set to indicate a timeout.
```