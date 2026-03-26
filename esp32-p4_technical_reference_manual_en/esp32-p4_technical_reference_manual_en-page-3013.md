

```markdown
Chapter 61 Temperature Sensor (TSENS)

Figure 61.3-1. Temperature Sensor Architecture

As Figure 61.3-1 shows, the temperature sensor module contains the following major blocks:

*   Tsens Ctrl & Detect: temperature sensor
*   HW Timer: triggers automatic temperature monitoring
*   Tsens_data Monitor: monitors whether the temperature is outside the threshold range
*   sync_module: Synchronization block between APB clock domain and temperature sensor clock domain

61.4 Functional Description

61.4.1 Temperature Sensor Power Up

The temperature sensor can be powered up by setting the TSENS_POWER_UP register.

61.4.2 Temperature Sensor Clock

The temperature sensor has only one clock source: LP_PERI_CLK, and there is no frequency divider inside the module.

61.4.3 Wake-Up Modes for Automatic Temperature Monitoring

There are two wake-up modes for temperature monitoring, selected by TSENS_WAKEUP_MODE:

*   Absolute value mode:
```