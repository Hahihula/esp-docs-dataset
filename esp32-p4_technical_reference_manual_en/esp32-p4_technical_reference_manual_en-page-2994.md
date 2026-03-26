

```markdown
Register 60.5. RTC_TOUCH_CHN_STATUS_REG (0x0010)

RTC_TOUCH_PAD_ACTIVE Indicates whether the touch pin detects a touch. Bit 1-14 corresponds to touch pin 1-14 respectively. Other bits are invalid.
0: No touch detected
1: Touch detected
(RO)

RTC_TOUCH_MEAS_DONE Indicates whether the touch pins have been measured at all frequency modes.
0: Not completed
1: Completed
(RO)

RTC_TOUCH_SCAN_CURR Indicates the index number of the currently scanned touch pin. (RO)
```

```markdown
Register 60.6. RTC_TOUCH_STATUS_n_REG (n: 1-14) (0x0018+0x4*(n-1))

RTC_TOUCH_PADn_DATA Indicates the touch_raw_data, touch_smooth_data, or benchmark sampled by touch pin n. (RO)

RTC_TOUCH_PADn_DEBOUNCE_CNT Indicates the cumulative number of consecutive touch or touch release detection by touch pin n. (RO)

RTC_TOUCH_PADn_NN_CNT Indicates the cumulative number of consecutive instances where touch_smooth_data < benchmark - passive_noise_threshold has been detected by touch pin n. (RO)
```