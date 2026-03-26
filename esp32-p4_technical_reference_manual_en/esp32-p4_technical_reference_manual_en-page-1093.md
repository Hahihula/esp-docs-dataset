

```markdown
9. Stop the timer (on final alarm iteration).
- Disable the ETM channels used to map timer group's event and task
- Set TIMER_ETM_EN to 0.
- Clear the interrupt by setting the timer's corresponding bit in TIMG_TO_INT_CLR.
- Disable the timer by clearing TIMG_TO_EN.

16.4.5 RTC_SLOW_CLK Frequency Calculation

1. One-shot frequency calculation
    - Configure HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_EN to enable clock gate of TIMGO_CALI_CLK.
    - Configure HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_SRC_SEL to select one clock as the clock source of TIMGO_CALI_CLK.
    - Configure HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_DIV_NUM to output TIMGO_CALI_CLK after integer prescaler.
    - Configure the time of calculation via TIMG_RTC_CALI_MAX.
    - Select one-shot frequency calculation by clearing TIMG_RTC_CALI_START_CYCLING, and enable the two counters via TIMG_RTC_CALI_START.
    - Once TIMG_RTC_CALI_RDY becomes 1, read TIMG_RTC_CALI_VALUE to get the value of XTAL_CLK's counter, and calculate the frequency of RTC_SLOW_CLK according to the formula in Section 16.3.6.

2. Periodic frequency calculation
    - Select the clock whose frequency is to be calculated (clock source of RTC_SLOW_CLK) via HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_SRC_SEL, and configure the time of calculation via TIMG_RTC_CALI_MAX.
    - Select periodic frequency calculation by enabling TIMG_RTC_CALI_START_CYCLING.
    - When TIMG_RTC_CALI_CYCLING_DATA_VLD is 1, TIMG_RTC_CALI_VALUE is valid.

3. Timeout
If the counter of RTC_SLOW_CLK cannot finish counting in TIMG_RTC_CALI_TIMEOUT_RST_CNT cycles, TIMG_RTC_CALI_TIMEOUT will be set to indicate a timeout.
```