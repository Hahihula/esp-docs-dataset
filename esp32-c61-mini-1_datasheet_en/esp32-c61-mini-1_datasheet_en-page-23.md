**Title: Peripherals**

---

### **5.2.2 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.

#### **5.2.2.1 SAR ADC**

ESP32-C61 integrates a Successive Approximation Analog-to-Digital Converter (SAR ADC) to convert analog signals into digital representations.

**Feature List**
- 12-bit sampling resolution
- Analog voltage sampling from up to four pins
- Attenuation of input signals for voltage conversion
- Software-triggered one-time sampling
- Timer-triggered multi-channel scanning
- DMA continuous conversion for seamless data transfer
- Two filters with configurable filter coefficient
- Threshold monitoring which helps to trigger an interrupt
- Support for Event Task Matrix

**Pin Assignment**

The SAR ADC pins are multiplexed with GPIO1 and GPIO3 ~ GPIO5. These GPIOs are also multiplexed with LP_GPIO1, LP_GPIO3 ~ LP_GPIO5, and the JTAG interface.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

---

### **5.2.2.2 Temperature Sensor**

The Temperature Sensor in the ESP32-C61 chip allows for real-time monitoring of temperature changes inside the chip.

**Feature List**
- Measurement range: -40°C ~ 125°C
- Software triggering, wherein the data can be read continuously once triggered
- Hardware automatic triggering and temperature monitoring
- Configurable temperature offset based on the environment to improve accuracy
- Adjustable measurement range
- Two automatic monitoring wake-up modes: absolute value mode and incremental value mode
- Support for Event Task Matrix

---

**Footer:**  
Espressif Systems  
23  
[Submit Documentation Feedback](#)  
ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6