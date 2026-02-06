Title: Peripherals

Subtitle: 5.2.2.1 SAR ADC

Body Text:
ESP8685 integrates two 12-bit SAR ADCs.

- ADC1 supports measurements on 5 channels, and is factory-calibrated.
- ADC2 supports measurements on 1 channel, and is not factory-calibrated.

Note Box (with border):
ADC2 of some chip revisions is not operable. For details, please refer to ESP32-C3 Series SoC Errata.

For more details, see ESP32-C3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing.

Subtitle: Pin Assignment

Body Text:
For details, see ESP8685 Series Datasheet > Section Peripheral Pin Assignment.

Title: 5.2.2.2 Temperature Sensor

Body Text:
The temperature sensor generates a voltage that varies with temperature. The voltage is internally converted via an ADC into a digital value.

The temperature sensor has a range of -40 °C to 125 °C. It is designed primarily to sense the temperature changes inside the chip. The temperature value depends on factors like microcontroller clock frequency or I/O load. Generally, the chip’s internal temperature is higher than the operating ambient temperature.

For more details, see ESP32-C3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing.

Footer:
Espressif Systems
Page Number: 20

Link Text at Bottom Right Corner (blue text): Submit Documentation Feedback