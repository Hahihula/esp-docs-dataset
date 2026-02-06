**Title: Peripherals**

---

### **5.2.2.1 SAR ADC**

ESP32-S3 integrates two 12-bit SAR ADCs and supports measurements on 20 channels (analog-enabled pins). For power-saving purpose, the ULP coprocessors in ESP32-S3 can also be used to measure voltage in sleep modes. By using threshold settings or other methods, we can awaken the CPU from sleep modes.

For more details, see [ESP32-S3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing](#).

---

### **Pin Assignment**

The pins for the SAR ADC are multiplexed with GPIO1 ~ GPIO20, RTC_GPIO1 ~ RTC_GPIO20, Touch Sensor interface, SPI interface, UART interface, and USB_D- and USB_D+ pins via IO MUX.

For more information about the pin assignment, see [ESP32-S3 Series Datasheet > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

### **5.2.2.2 Temperature Sensor**

The temperature sensor generates a voltage that varies with temperature. The voltage is internally converted via an ADC into a digital value.

The temperature sensor has a range of -40 °C to 125 °C. It is designed primarily to sense the temperature changes inside the chip. The temperature value depends on factors such as microcontroller clock frequency or I/O load. Generally, the chip's internal temperature is higher than the ambient temperature.

For more details, see [ESP32-S3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing](#).

---

### **5.2.2.3 Touch Sensor**

ESP32-S3 has 14 capacitive-sensing GPIOs, which detect variations induced by touching or approaching the GPIOs with a finger or other objects. The low-noise nature of the design and the high sensitivity of the circuit allow relatively small pads to be used. Arrays of pads can also be used, so that a larger area or more points can be detected. The touch sensing performance can be further enhanced by the waterproof design and digital filtering feature.

**Note:**
ESP32-S3 touch sensor has not passed the Conducted Susceptibility (CS) test for now, and thus has limited application scenarios.
For more details, see [ESP32-S3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing](#).

---

### **Pin Assignment**

The pins for touch sensor are multiplexed with GPIO1 ~ GPIO14, RTC_GPIO1 ~ RTC_GPIO14, SAR ADC interface, and SPI interface via IO MUX.

For more information about the pin assignment, see [ESP32-S3 Series Datasheet > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Footer:**
Espressif Systems  
Page 28  
[Submit Documentation Feedback](#)