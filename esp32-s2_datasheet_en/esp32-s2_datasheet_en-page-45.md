**Title: Functional Description**

CPU is in Deep-sleep mode, which lowers the total power consumption. By using threshold settings, and / or via other triggers or events, we can interrupt the CPU from the sleep state.

The ADCs can be configured to measure voltage on up to 20 pins.
For ADC characteristics, please refer to Table 5.5 ADC Characteristics.

**Subtitle: Pin Assignment**

For details, see Section [2.3.6 Peripheral Pin Assignment](#).

---

**Title: DAC (4.2.2.2)**

ESP32-S2 has two 8-bit DAC channels that convert two digital signals into two analog voltage signal outputs.
The two DAC channels support independent conversions. The design structure is composed of integrated resistor strings and a buffer. This dual DAC supports VDD3P3_RTC_IO power supply as input voltage reference.

**Subtitle: Pin Assignment**

For details, see Section [2.3.6 Peripheral Pin Assignment](#).

---

**Title: Temperature Sensor (4.2.2.3)**

The temperature sensor generates a voltage that varies with temperature.
The voltage is internally converted via an ADC into a digital value.

The temperature sensor has a range of –20 °C to 110 °C. It is designed primarily to sense the temperature changes inside the chip. The temperature value depends on factors like microcontroller clock frequency or I/O load. Generally, the chip’s internal temperature is higher than the ambient operating temperature.

---

**Title: Touch Sensor (4.2.2.4)**

ESP32-S2 has 14 capacitive-sensing GPIOs, which detect variations induced by touching or approaching the GPIOs with a finger or other objects.
The low-noise nature of the design and the high sensitivity of the circuit allow relatively small pads to be used. Arrays of pads can also be used, so that a larger area or more points can be detected.

The touch sensing performance can be further enhanced by the waterproof design and digital filtering feature.

**Note:**
ESP32-S2 Touch Sensor has not passed the Conducted Susceptibility (CS) test for now, and thus has limited application scenarios.
For details, see Section [2.3.6 Peripheral Pin Assignment](#).

---

**Title: Pin Assignment**

Espressif Systems
45 ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback]