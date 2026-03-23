

# Chapter 39 ## On-Chip Sensor and Analog Signal Processing

### 39.1 Overview

ESP32-C6 provides the following on-chip sensor and analog signal processing peripherals:

*   One 12-bit Successive Approximation ADC (SAR ADC) for measuring analog signals from seven channels;
*   One temperature sensor for measuring the internal temperature of the ESP32-C6 chip.

### 39.2 SAR ADC

#### 39.2.1 Overview

ESP32-C6 integrates a 12-bit SAR ADC which is able to measure analog signals from up to seven pins. It is also possible to measure internal signals, such as VDD33. The SAR ADC is managed by the DIG ADC controller, which drives the Digital_reader to sample channel voltages by SAR ADC. It supports high-performance multi-channel scanning and DMA continuous conversion.

#### 39.2.2 Features

*   12-bit sampling resolution
*   Analog voltage sampling from up to seven pins
*   DIG ADC controller:

    *   Separate control modules for one-time sampling and multi-channel scanning
    *   Configurable channel scanning sequence in multi-channel scanning mode
    *   Two filters with configurable filter coefficient
    *   Threshold monitoring, which helps to trigger an interrupt when the sampled value is greater than the pre-set high threshold or less than the pre-set low threshold
    *   DMA

#### 39.2.3 Functional Description

The major components of SAR ADC and their interconnections are shown in Figure 39.2-1.