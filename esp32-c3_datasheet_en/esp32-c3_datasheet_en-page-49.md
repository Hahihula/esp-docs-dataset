**Title: Functional Description**

- **Can generate digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 14 bits.**
- Has multiple clock sources, including APB clock and external main crystal clock.
- Can operate when the CPU is in Light-sleep mode.

Supports gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator.

For details, see [ESP32-C3 Technical Reference Manual > Chapter LED PWM Controller](#).

---

**Title: Pin Assignment**

For details, see Section 2.3.4 Peripheral Pin Assignment.

---

### Subtitle: Remote Control Peripheral

#### Section Number and Title:
4.2.1.8 Remote Control Peripheral

The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols. All four channels share a 192 x 32-bit memory block to store transmit or receive waveform.

For more details, see [ESP32-C3 Technical Reference Manual > Chapter Remote Control Peripheral (RMT)](#).

---

**Title: Pin Assignment**

For details, see Section 2.3.4 Peripheral Pin Assignment.

---

### Subtitle: Analog Signal Processing

#### Section Number and Title:
4.2.2 Analog Signal Processing

This subsection describes components on the chip that sense and process real-world data.

#### Subsection:

4.2.2.1 SAR ADC

ESP32-C3 integrates two 12-bit SAR ADCs.
- ADC1 supports measurements on 5 channels, and is factory-calibrated.
- ADC2 supports measurements on 1 channel, and is not factory-calibrated.

**Note:**
ADC2 of some chip revisions is not operable. For details, please refer to [ESP32-C3 Series SoC Errata](#).

For ADC characteristics, please refer to Section 5.5 ADC Characteristics.
For more details, see [ESP32-C3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing](#).

---

**Footer:**
Espressif Systems  
49  
[Submit Documentation Feedback](#)  
ESP32-C3 Series Datasheet v2.2