

# Chapter 34

## On-Chip Sensor and Analog Signal Processing

### 34.1 Overview

ESP32-C3 provides the following on-chip sensor and analog signal processing peripherals:

- Two 12-bit Successive Approximation ADCs (SAR ADCs): SAR ADC1 and SAR ADC2, for measuring analog signals from six channels.
- One temperature sensor for measuring the internal temperature of the ESP32-C3 chip.

### 34.2 SAR ADCs

#### 34.2.1 Overview

ESP32-C3 integrates two 12-bit SAR ADCs, which are able to measure analog signals from up to six pins. The SAR ADCs are managed by two dedicated controllers:

- DIG ADC controller: drives Digital_Reader0 and Digital_Reader1 to sample channel voltages of SAR ADC1 and SAR ADC2, respectively. This DIG ADC controller supports high-performance multi-channel scanning and DMA continuous version.
- PWDDET controller: monitors RF power. Note this controller is only for RF internal use.

**Note:**  
The DIG ADC controller of SAR ADC2 for ESP32-C3 does not work properly and it is suggested to use SAR ADC1. For more information, please refer to ESP32-C3 Series SoC Errata.

#### 34.2.2 Features

- Each SAR ADC has its own ADC Reader module (Digital_Reader0 or Digital_Reader1), which can be configured and operated separately.
- Support 12-bit sampling resolution
- Support sampling the analog voltages from up to six pins
- DIG ADC controller:
    - Provides separate control modules for one-time sampling and multi-channel scanning.
    - One-time sampling and multi-channel scanning can be run independently on each ADC.
    - Channel scanning sequence in multi-channel scanning mode is user-defined.