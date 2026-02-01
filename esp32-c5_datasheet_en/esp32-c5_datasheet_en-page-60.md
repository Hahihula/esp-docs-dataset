**Title: Functional Description**

- **Bullet Point:** support for several Event Task Matrix (ETM) related events and tasks

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter ADC Controller.

---

**Subtitle: Pin Assignment**

The pins for the ADC controller are multiplexed with GPIO1 ~ GPIO6. For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Title: 4.2.2.3 Analog Voltage Comparator**

ESP32-C5 provides an analog voltage comparator which contains two special pads. This peripheral can be used to compare the voltages of the two pads or compare the voltage of one pad with a stable internal voltage that is adjustable.

**Subtitle: Feature List**
- **Bullet Point:** internal or external reference voltage
- **Bullet Point:** supported internal reference voltage ranging from 0 to 0.7 * VDD_PST
- **Bullet Point:** support for ETM
- **Bullet Point:** interrupt triggered when the measured voltage reaches the reference voltage

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Analog Voltage Comparator.

---

**Subtitle: Pin Assignment**

The analog voltage comparator has dedicated pads, GPIO8 and GPIO9. GPIO9 is the test pad, and GPIO8 serves as the reference pad when using an external reference voltage.
For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Footer:**
- Espressif Systems
- Page number: 60
- Document title: ESP32-C5 Series Datasheet v1.0

[Submit Documentation Feedback](#)