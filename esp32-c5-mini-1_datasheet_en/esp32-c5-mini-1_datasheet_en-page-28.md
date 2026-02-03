**Title: Peripherals**

---

### Feature List

- **12-bit resolution**
- analog inputs sampling from up to six pins
- one-shot sampling mode and multi-channel sampling mode
- multi-channel sampling mode supports:
  - configurable channel sampling sequence
  - two filters whose filter coefficients are configurable
  - two threshold monitors that can trigger an interrupt when the filtered value is below a low threshold or above a high threshold
  - continuous transfer of converted data to memory via GDMA interface
- support for several Event Task Matrix (ETM) related events and tasks

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter ADC Controller.

---

### Pin Assignment

The pins for the ADC controller are multiplexed with GPIO1 ~ GPIO6. For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section 10 Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

### Subsection: 5.2.2.3 Analog Voltage Comparator

ESP32-C5 provides an analog voltage comparator which contains two special pads. This peripheral can be used to compare the voltages of the two pads or compare the voltage of one pad with a stable internal voltage that is adjustable.

#### Feature List
- **internal or external reference voltage**
  - supported internal reference voltage ranging from 0 to 0.7 * VDD_PST
- support for ETM
- interrupt triggered when the measured voltage reaches the reference voltage

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Analog Voltage Comparator.

#### Pin Assignment

The analog voltage comparator has dedicated pads, GPIO8 and GPIO9. GPIO9 is the test pad, and GPIO8 serves as the reference pad when using an external reference voltage.
For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section 10 Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-C5-MINI-1 Datasheet v1.0