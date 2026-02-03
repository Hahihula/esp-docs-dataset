**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Note Section (with bullet points):**
- When the arbiter is masked, only one of the above APB_SARADC_ADC_ARB_XXX_FORCED bits can be set to 1.
- The arbiter uses APB_CLK as its clock source. When the clock frequency is 8 MHz or lower, the arbiter must be masked.

**Subsection Title:**
39.4 Temperature Sensor

**Sub-subsection (with subheading and text):**
39.4.1 Overview
ESP32-S3 provides a temperature sensor to monitor temperature changes inside the chip in real time.

**Sub-subsection with Subtitle & List of Features:**
39.4.2 Features
The temperature sensor has the following features:
- Monitored in real time by ULP coprocessor when in low-power mode.
- Triggered by software or by ULP coprocessor.
- Configurable temperature offset based on the environment, to improve the accuracy.
- Adjustable measurement range.

**Footer:**
Espressif Systems
Page Number 1475 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback