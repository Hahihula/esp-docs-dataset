**Title: Functional Description**

- DMA continuous conversion for seamless data transfer
- Two filters with configurable filter coefficient
- Threshold monitoring which helps to trigger an interrupt
- Support for Event Task Matrix

---

**Subtitle: Pin Assignment**

The SAR ADC pins are multiplexed with GPIO1 and GPIO3 ~ GPIO5. These GPIOs are also multiplexed with LP_GPIO1, LP_GPIO3 ~ LP_GPIO5, and with the JTAG interface.

For more information about the pin assignment, see Section 2.3 IO Pins.

---

**Subtitle: Temperature Sensor (4.2.2.2)**

The Temperature Sensor in the ESP32-C61 chip allows for real-time monitoring of temperature changes inside the chip.

**Feature List**
- Measurement range: -40°C ~ 125°C
- Software triggering, wherein the data can be read continuously once triggered
- Hardware automatic triggering and temperature monitoring
- Configurable temperature offset based on the environment to improve the accuracy
- Adjustable measurement range
- Two automatic monitoring wake-up modes: absolute value mode and incremental value mode
- Support for Event Task Matrix

---

**Subtitle: Analog Voltage Comparator (4.2.2.3)**

ESP32-C61 provides a group of analog voltage comparators which contain two special pads. This peripheral can be used to compare the voltages of the two pads or compare the voltage of one pad with an internally adjustable stable voltage.

**Feature List**
- Internal or external reference voltage
- Supported internal reference voltage ranging from 0 to 0.7 x VDD_PST
- Support for ETM
- Interrupt triggered when the measured voltage reaches the reference voltage

**Pin Assignment**

The analog voltage comparator has dedicated pads, GPIO8 and GPIO9. GPIO9 is the test pad, and GPIO8 serves as the reference pad when using an external reference voltage.

---

**Footer:**
Espressif Systems  
49 ESP32-C61 Series Datasheet v0.5