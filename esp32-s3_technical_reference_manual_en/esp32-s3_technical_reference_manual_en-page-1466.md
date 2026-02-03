**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Body Text with List Items (Note Section):**
- Two RTC controllers: RTC ADC1 controller and RTC ADC2 controller, designed for single conversion mode and low power mode.
- One internal controller: Power/Peak Detect Controller (PWDET controller), designed to monitor RF power. Note this controller is only for RF internal use.

**Note Box Content:** 
The DIG ADC2 controller of ESP32-S3 doesn’t work properly and related information has been deleted in this chapter. For more information, please refer to ESP32-S3 Series SoC Errata.

**Subsection Title:**
39.3.2 Features

**Body Text with List Items (Features Section):**
The SAR ADC module has the following features:
- Each SAR ADC controller has its own ADC Reader module. See Figure 39.3-2.
- Support DIG ADC1 controller and RTC ADC1 controller to get the control of SAR ADC1 via software.
- Support RTC ADC2 controller and PWDET controller to get the control of SAR ADC2 by the specified arbitration method via the arbiter.
- Support 12-bit sampling resolution
- Support sampling the analog voltages from up to 20 pins

**Subsection Title:**
RTC ADC1/2 controllers, with the following features:
- Support single conversion mode
- Support working in low power mode, such as in Deep-sleep mode
- Configurable by the ULP coprocessor

**Subsection Title:**
DIG ADC1 controller, with the following features:

- Support multi-channel scanning
- Provide a mode control module, supporting single SAR ADC sampling mode
- Configurable scanning sequence in multi-channel scanning mode
- Provide two filters with configurable coefficient
- Support threshold monitoring. An interrupt will be triggered when the sampled value is greater than the pre-set high threshold or less than the pre-set low threshold.
- Support DMA

**Subsection Title:**
PWDET controller: monitor RF power. Note this controller is only for RF internal use.

**Subsection Title:**
39.3.3 SAR ADC Architecture

**Body Text with Reference to Figure:** 
The major components of SAR ADCs and their interconnections are shown in Figure 39.3-2.

**Footer Information:**
Espressif Systems
1466 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback