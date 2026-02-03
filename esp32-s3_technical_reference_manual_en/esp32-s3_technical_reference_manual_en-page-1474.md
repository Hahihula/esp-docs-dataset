**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Section Header:**
The configuration of threshold monitoring is as follows:

- **Set APB_SARADC_THRESx_EN**: to enable threshold monitor x.
- **Configure APB_SARADC_THRESx_LOW**: to set a low threshold.
- **Configure APB_SARADC_THRESx_HIGH**: to set a high threshold.

**Note:**
Note that x is used here as the placeholder of monitor index. 0: monitor 0; 1: monitor 1.

---

**Subsection Title:**
39.3.8 SAR ADC2 Arbiter

**Body Text:**
SAR ADC2 can be controlled by two controllers, namely, RTC ADC2 controller and PWDET controller. To avoid any possible conflicts and to improve the efficiency of SAR ADC2, ESP32-S3 provides an arbiter for SAR ADC2. The arbiter supports fair arbitration and fixed priority arbitration.

- **Fair arbitration mode (cyclic priority arbitration)** can be enabled by clearing APB_SARADC_ADC_ARB_FIX.
- In fixed priority arbitration, users can set APB_SARADC_ADC_ARB_RTC_PRIORITY (for RTC ADC2 controller) or APB_SARADC_ADC_ARB_WIFI_PRIORITY (for PWDET controller), to configure the priorities for these controllers. A larger value indicates a higher priority.

The arbiter ensures that a higher priority controller can always start a conversion (sample) when required, regardless of whether a lower priority controller already has a conversion in progress. If a higher priority controller starts a conversion whilst the ADC already has a conversion in progress from a lower priority controller, the conversion in progress will be interrupted (stopped). The highest priority controller will then start its conversion. A lower priority controller will not be able to start a conversion whilst the ADC has a conversion in progress from a higher priority controller.

Therefore, certain data flags are embedded into the output data value to indicate whether the conversion is valid or not.
- **The data flag for RTC ADC2 controller** is the higher two bits of SENS_MEMAS2_DATA_SAR:
  - `2'b10`: Conversion is interrupted.
  - `2'b01`: Conversion is not started.
  - `2'b00`: The data is valid.

- **The data flag for PWDET controller** is the higher two bits of the sampling result:
  - `2'b10`: Conversion is interrupted.
  - `2'b01`: Conversion is not started.
  - `2'b00`: The data is valid.

Users can configure APB_SARADC_ADC_ARB_GRANT FORCE to mask the arbiter, and set APB_SARADC_ADC_ARB_WIFI_FORCE or APB_SARADC_ADC_ARB_RTC_FORCE to authorize corresponding controllers. 

**Footer:**
Espressif Systems
1474 ESP32-S3 TRM (Version 1.7)