**Title:**
5 Peripherals

**Subtitle:**
5.2.2.3 Analog Voltage Comparator

**Body Text:**
ESP32-C61 provides a group of analog voltage comparators which contain two special pads. This peripheral can be used to compare the voltages of the two pads or compare the voltage of one pad with an internally adjustable stable voltage.

**Feature List:**
- Internal or external reference voltage
- Supported internal reference voltage ranging from 0 to 0.7 × VDD_PST
- Support for ETM
- Interrupt triggered when the measured voltage reaches the reference voltage

**Subsection Title:**
Pin Assignment

**Subsection Text:**
The analog voltage comparator has dedicated pads, GPIO8 and GPIO9. GPIO9 is the test pad, and GPIO8 serves as the reference pad when using an external reference voltage.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Information:**
ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6