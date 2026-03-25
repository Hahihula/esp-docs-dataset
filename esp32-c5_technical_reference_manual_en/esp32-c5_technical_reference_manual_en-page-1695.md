

```markdown
- Monitors the absolute value of the current temperature. Configure APB_SARADC_WAKEUP_TH_LOW and APB_SARADC_WAKEUP_TH_HIGH to set the temperature thresholds. An interrupt will be triggered if the sampled value is above the high threshold or below the low threshold.
- Change value mode:
  - Monitors the temperature changes inside the chip. If the temperature increment of two consecutive samplings exceeds the high threshold configured in APB_SARADC_WAKEUP_TH_HIGH, or the temperature decrement of two consecutive samplings exceeds the low threshold configured in APB_SARADC_WAKEUP_TH_LOW, an interrupt will be triggered. For example, when APB_SARADC_WAKEUP_TH_LOW is configured as 8, if two consecutive sampling values are 28 and 19 respectively, i.e., the temperature decrement is 9, then an interrupt will be triggered.

## 45.4.4 Temperature Measurement Range and Offset

To improve the temperature measurement accuracy, the temperature sensor is designed with five measurement ranges as shown in Table 45.4-1. Each measurement range comes with specific measurement errors. Users do not need to worry about the errors, as they can choose specific offsets to get calibrated data.

**Table 45.4-1. Temperature Measurement Range and Offset**

| Temperature Measurement Range (°C) | Temperature Offset |
|------------------------------------|--------------------|
| 50 ~ 125                           | -2                 |
| 20 ~ 100                           | -1                 |
| -10 ~ 80                           | 0                  |
| -30 ~ 50                           | 1                  |
| -40 ~ 20                           | 2                  |

## 45.4.5 Data Conversion

The sensor output value is stored in APB_SARADC_TSENS_OUT. To calculate the actual temperature T (°C) based on VALUE, use the following equation:

```math
T = 0.4386 * VALUE - 27.88 * offset - 20.52
```

where `offset` is the temperature offset shown in Table 45.4-1.

## 45.5 Programming Procedure

The temperature sensor can be started by software as follows:

1. Set APB_SARADC_TSENS_PU to power up the temperature sensor.
2. Set PCR_TSENS_CLK_EN to enable the temperature sensor clock.
3. Configure APB_SARADC_TSENS_CLK_SEL to select the temperature sensor clock.
4. Wait for APB_SARADC_TSENS_XPD_WAIT clock cycles till the temperature sensor releases from reset and starts measuring the temperature.
```