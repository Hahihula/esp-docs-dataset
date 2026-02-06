**Title: Peripherals**

---

### **5.2.1.8 Remote Control Peripheral**

The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols. All four channels share a 192 x 32-bit memory block to store transmit or receive waveform.

For more details, see [ESP32-C3 Technical Reference Manual > Chapter Remote Control Peripheral (RMT)](#).

---

### **Pin Assignment**

The pins for the Remote Control Peripheral can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-C3 Series Datasheet > Section IO Pins and ESP32-C3 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix](#).

---

### **5.2.2 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.

---

### **5.2.2.1 SAR ADC**

ESP32-C3 integrates two 12-bit SAR ADCs.
- ADC1 supports measurements on 5 channels, and is factory-calibrated.
- ADC2 supports measurements on 1 channel, and is not factory-calibrated.

**Note:**  
ADC2 of some chip revisions is not operable. For details, please refer to [ESP32-C3 Series SoC Errata](#).

For more details, see [ESP32-C3 Technical Reference Manual > Chapter On-Chip Sensors and Analog Signal Processing](#).

---

### **Pin Assignment**

The pins for the SAR ADC are multiplexed with GPIO0 ~ GPIO5, JTAG interface, SPI2 interface, and pins for external crystal or oscillator.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet > Section IO Pins and ESP32-C3 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix](#).

---

### **5.2.2.2 Temperature Sensor**

The temperature sensor generates a voltage that varies with temperature. The voltage is internally converted via an ADC into a digital value.

The temperature sensor has a range of -40 °C to 125 °C. It is designed primarily to sense the temperature changes inside the chip. The temperature value depends on factors like microcontroller clock frequency or I/O load. Generally, the chip's internal temperature is higher than the operating ambient temperature.

---

**Footer:**  
Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6

Page 20