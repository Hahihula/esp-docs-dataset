

```markdown
- Set `APB_SARADC_TSENS_CPU` to start XPD_SAR and to enable the temperature sensor; Set `PCR_TSENS_CLK_EN` to enable the temperature sensor clock;
- Wait for `APB_SARADC_TSENS_XPD_WAIT` clock cycles till the reset of the temperature sensor is released, then the sensor starts measuring the temperature;
- Wait for a while and then read the data from `APB_SARADC_TSENS_OUT`. The output value gradually approaches the actual temperature linearly as the measurement time increases.

The temperature sensor can also be automatically triggered to continuously monitor the temperature as follows:

- Set `APB_SARADC_TSENS_CPU` to start XPD_SAR and to enable the temperature sensor; Set `PCR_TSENS_CLK_EN` to enable the temperature sensor clock;
- Wait for `APB_SARADC_TSENS_XPD_WAIT` clock cycles till the reset of the temperature sensor is released, then the sensor starts measuring the temperature;
- Configure `APB_SARADC_TSENS_SAMPLE_RATE` to set sample rate;
- Set `APB_SARADC_WAKEUP_MODE` to enable temperature monitor mode;
- Set `APB_SARADC_WAKEUP_EN` to enable temperature monitoring;
- Set `APB_SARADC_TSENS_SAMPLE_EN` to automatically start continuous temperature monitoring.

There are two wake-up modes for the temperature sensor to start automatic monitor:

* Absolute value mode:
  - Monitors the absolute value of the current temperature. Configure `APB_SARADC_WAKEUP_TH_LOW` and `APB_SARADC_WAKEUP_TH_HIGH` to set the temperature thresholds. Wake-up will be triggered if the sampled value exceeds the high threshold or is less than the low threshold.
* Incremental value mode:
  - Monitors the incremental value of the current temperature. If the temperature increment of two consecutive samplings exceeds the high threshold configured in `APB_SARADC_WAKEUP_TH_HIGH` or the temperature decrement of two consecutive samplings exceeds the low threshold configured in `APB_SARADC_WAKEUP_TH_LOW`, a wake-up will be triggered. For example, when `APB_SARADC_WAKEUP_TH_LOW` is configured as 8, if two consecutive sampling values are 28 and 19 respectively, i.e., the temperature decrement is 9, then a wake-up will be triggered.

The actual temperature (°C) can be obtained by converting the output of temperature sensor via the following formula:

```math
T(^\circ C) = 0.4386 \times VALUE - 27.88 \times offset - 20.52
```

VALUE in the formula is the output of the temperature sensor, and the offset is determined by the temperature offset. The temperature offset varies in different actual environment (the temperature range). For details, refer to Table 39.3-1.

Table 39.3-1. Temperature Offset

| Measurement Range (°C) | Temperature Offset (°C) |
|------------------------|-------------------------|
| 50 ~ 125               | -2                      |
| 20 ~ 100               | -1                      |
```