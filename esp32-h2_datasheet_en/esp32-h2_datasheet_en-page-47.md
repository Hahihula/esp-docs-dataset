**Title: Functional Description**

---

### Pin Assignment

The pins for the Remote Control Peripheral can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

#### Subtitle: 4.2.1.11 Parallel IO Controller

The Parallel IO Controller (PARLIO) in the ESP32-H2 chip enables data transfer between external devices and internal memory on a parallel bus through GDMA. It consists of a transmitter (TX unit) and a receiver (RX unit), making it a versatile interface for connecting various peripherals.

**Feature List**
- 1/2/4/8-bit configurable data bus width
- Full-duplex communication with 8-bit data bus width
- Bit reordering in 1/2/4-bit data bus width mode
- RX unit supports eight receive modes categorized into three major categories: Level Enable mode, Pulse Enable mode, and Software Enable mode
- TX unit can generate a valid signal aligned with TXD

For details, see ESP32-H2 Technical Reference Manual > Chapter Parallel IO Controller.

---

### Pin Assignment (Repeated)

The pins for the Parallel IO Controller can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

#### Subtitle: 4.2.2 Analog Signal Processing

This subsection describes components on the chip that sense and process real-world data.

##### Subsection Title: 4.2.2.1 SAR ADC

ESP32-H2 integrates a Successive Approximation Analog-to-Digital Converter (SAR ADC) to convert analog signals into digital representations.

**Feature List**
- 12-bit sampling resolution
- Analog voltage sampling from up to five pins
- Attenuation of input signals for voltage conversion
- Software-triggered one-time sampling
- Timer-triggered multi-channel scanning

---

Espressif Systems  
47  
ESP32-H2 Series Datasheet v1.2  

[Submit Documentation Feedback](#)