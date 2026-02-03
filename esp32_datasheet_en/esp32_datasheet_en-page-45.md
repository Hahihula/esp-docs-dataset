Title: Functional Description

- Bullet Point:
  The input voltage range of GPIO pins within VDD3P3_RTC domain should strictly follow the DC characteristics provided in Table 5-3. Otherwise, measurement errors may be introduced, and chip performance may be affected.

Body Text:

By default, there are ±6% differences in measured results between chips. ESP-IDF provides couple of calibration methods for ADC1. Results after calibration using eFuse Vref value are shown in Table 4-4. For higher accuracy, users may apply other calibration methods provided in ESP-IDF, or implement their own.

Subtitle: Table 4-4. ADC Calibration Results

Table:
| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| Total error | Atten = 0, effective measurement range of 100 ~ 950 mV | -23 | 23 | mV |
| | Atten = 1, effective measurement range of 100 ~ 1250 mV | -30 | 30 | mV |
| | Atten = 2, effective measurement range of 150 ~ 1750 mV | -40 | 40 | mV |
| | Atten = 3, effective measurement range of 150 ~ 2450 mV | -60 | 60 | mV |

For details, see ESP32 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing.

Subtitle: Pin Assignment

Body Text:

With appropriate settings, the ADCs can be configured to measure voltage on 18 pins maximum. For detailed information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

Title: Digital-to-Analog Converter (DAC)

Subtitle:
4.9.2

Body Text:

Two 8-bit DAC channels can be used to convert two digital signals into two analog voltage signal outputs. The design structure is composed of integrated resistor strings and a buffer. This dual DAC supports power supply as input voltage reference. The two DAC channels can also support independent conversions.

For details, see ESP32 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing.

Subtitle: Pin Assignment

Body Text:

The DAC can be configured by GPIO 25 and GPIO 26. For detailed information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

Title:
4.9.3 Touch Sensor

Body Text:

ESP32 has 10 capacitive-sensing GPIOs, which detect variations induced by touching or approaching the GPIOs with a finger or other objects. The low-noise nature of the design and the high sensitivity of the circuit allow relatively small pads to be used. Arrays of pads can also be used, so that a larger area or more points can be detected.

Footer:
Espressif Systems
45
Submit Documentation Feedback

ESP32 Series Datasheet v5.2