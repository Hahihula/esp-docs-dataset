

```markdown
Chapter 34 On-Chip Sensor and Analog Signal Processing

The arbiter ensures that a higher priority controller can always start a conversion (sample) when required, regardless of whether a lower priority controller already has a conversion in progress. If a higher priority controller starts a conversion whilst the ADC already has a conversion in progress from a lower priority controller, the conversion in progress will be interrupted (stopped). The higher priority controller will then start its conversion. A lower priority controller will not be able to start a conversion whilst the ADC has a conversion in progress from a higher priority controller.

Therefore, certain data flags are embedded into the output data value to indicate whether the conversion is valid or not.

*   The data flag for DIG ADC controller is the {sar_sel, ch_sel} bits in DMA data, see Figure 34.2-8.
    -   `4'b1111`: Conversion is interrupted.
    -   `4'b1110`: Conversion is not started.
    -   Corresponding channel No.: The data is valid.

*   The data flag for PWDET controller is the two higher bits of the sampling result.
    -   `2'b10`: Conversion is interrupted.
    -   `2'b01`: Conversion is not started.
    -   `2'b00`: The data is valid.

Users can configure APB_SARADC_ADC_ARB_GRANT_FORCE to mask the arbiter, and set APB_SARADC_ADC_ARB_WIFI_FORCE or APB_SARADC_ADC_ARB_APB_FORCE to authorize corresponding controllers.

34.3 Temperature Sensor

34.3.1 Overview

ESP32-C3 provides a temperature sensor to monitor temperature changes inside the chip in real time.

34.3.2 Features

The temperature sensor has the following features:

*   Supports software triggering and, once triggered, the data can be read continuously
*   Configurable temperature offset based on the environment, to improve the accuracy
*   Adjustable measurement range

34.3.3 Functional Description

The temperature sensor can be started by software as follows:

*   Set APB_SARADC_TSENS_PU to start XPD_SAR, and then to enable temperature sensor;
*   Set SYSTEM_TSENS_CLK_EN to enable temperature sensor clock;
*   Wait for APB_SARADC_TSENS_XPD_WAIT clock cycles till the reset of temperature sensor is released, the sensor starts measuring the temperature;
```