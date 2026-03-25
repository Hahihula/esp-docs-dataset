

```markdown
Chapter 13 Timer Group (TIMG) GoBack

2. Periodic frequency calculation

- Select the clock whose frequency is to be calculated (clock source of RTC_SLOW_CLK) via TIMGO_RTC_CALI_CLK_SEL, and configure the time of calculation via TIMGO_RTC_CALI_MAX.
- Select periodic frequency calculation by enabling TIMGO_RTC_CALI_START_CYCLING.
- When TIMGO_RTC_CALI_CYCLING_DATA_VLD is 1, TIMGO_RTC_CALI_VALUE is valid.

3. Timeout

If the counter of RTC_SLOW_CLK cannot finish counting in TIMGO_RTC_CALI_TIMEOUT_RST_CNT cycles, TIMGO_RTC_CALI_TIMEOUTT will be set to indicate a timeout.
```