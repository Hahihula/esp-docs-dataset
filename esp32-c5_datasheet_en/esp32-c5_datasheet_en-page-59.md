**Title: Functional Description**

For more information about the pin assignment, see Section **2.3 IO Pins** and ESP32-C5 Technical Reference Manual > Chapter IOMUX and GPIO Matrix.

---

**Note:**  
This peripheral is supported by chip revision v1.0, but not v0.1.

---

### 4.2.2 Analog Signal Processing

This subsection describes components on the chip that sense and process real-world data.

#### **4.2.2.1 Temperature Sensor**

ESP32-C5 provides a temperature sensor to monitor temperature changes inside the chip in real time. The sensor converts analog voltage to digital values and supports compensation for the temperature offset.

**Feature List**
- software-triggered temperature measurement. Once triggered, the sensor continuously measures temperature. Software can read the data any time.
- hardware-triggered automatic temperature monitoring
- two modes for automatic monitoring of temperature and support for triggering interrupts
- configurable temperature offset based on the application scenario for improved accuracy
- configurable temperature measurement range
- support for several Event Task Matrix (ETM) related events and tasks

For more details, see ESP32-C5 Technical Reference Manual > Chapter Temperature Sensor.

---

### 4.2.2.2 ADC Controller

ESP32-C5 integrates One 12-bit successive approximation ADC (SAR ADC) for measuring analog signals from up to six channels.

**Feature List**
- 12-bit resolution
- analog inputs sampling from up to six pins
- one-shot sampling mode and multi-channel sampling mode
- multi-channel sampling mode supports:
  - configurable channel sampling sequence
  - two filters whose filter coefficients are configurable
  - two threshold monitors that can trigger an interrupt when the filtered value is below a low threshold or above a high threshold
  - continuous transfer of converted data to memory via GDMA interface

---

Espressif Systems  
59  
ESP32-C5 Series Datasheet v1.0  

[Submit Documentation Feedback](#)