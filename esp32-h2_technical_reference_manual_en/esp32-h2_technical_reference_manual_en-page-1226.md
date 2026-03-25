

```markdown
Chapter 39 Temperature Sensor (TSENS)

GoBack

Figure 39.3-1. Temperature Sensor Architecture

As Figure 39.3-1 shows, the temperature sensor module contains the following major blocks:

* Tsens Ctrl & Detect: temperature sensor
* HW Timer: triggers automatic temperature monitoring
* Tsens_data Monitor: monitors whether the temperature is outside the threshold range
* sync_module: synchronization block between APB clock domain and temperature sensor clock domain

39.4 Functional Description

39.4.1 Temperature Sensor Power Up

The temperature sensor can be powered up by setting the `APB_SARADC_TSENS_PU` register.

39.4.2 Temperature Sensor Clock

The temperature sensor has two clock sources: RC_FAST_CLK and XTAL_CLK, selected by `PCR_TSENS_CLK_SEL`. The clock can be divided with `APB_SARADC_TSENS_CLK_DIV`.

39.4.3 Wake-Up Modes for Automatic Temperature Monitoring

There are two wake-up modes for the temperature monitoring, selected by configuring `APB_SARADC_WAKEUP_MODE`:

* Absolute value mode:
```