**Title: Functional Description**

---

### Pin Assignment

For details, see Section **2.3.5 Peripheral Pin Assignment**.

#### Subtitle: 4.2.1.12 Parallel IO Controller

The Parallel IO Controller (PARLIC) in the ESP32-C6 chip enables data transfer between external devices and internal memory on a parallel bus through GDMA. It consists of a transmitter (TX unit) and a receiver (RX unit), making it a versatile interface for connecting various peripherals.

**Feature List**
- 1/2/4/8/16-bit configurable data bus width
- Half-duplex communication with 16-bit data bus width and full-duplex communication with 8-bit data bus width
- Bit reordering in 1/2/4-bit data bus width mode
- RX unit supports 15 receive modes categorized into three major categories: Level Enable mode, Pulse Enable mode, and Software Enable mode
- TX unit can generate a valid signal aligned with TX

For more details, see **ESP32-C6 Technical Reference Manual** > Chapter Parallel IO Controller.

---

### Pin Assignment (Repeated)

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

#### Subtitle: 4.2.2 Analog Signal Processing

This subsection describes components on the chip that sense and process real-world data.

##### Subsection Title: 4.2.2.1 SAR ADC

ESP32-C6 integrates a Successive Approximation Analog-to-Digital Converter (SAR ADC) to convert analog signals into digital representations.

**Feature List**
- 12-bit sampling resolution
- Analog voltage sampling from up to seven pins
- Attenuation of input signals for voltage conversion
- Software-triggered one-time sampling
- Timer-triggered multi-channel scanning
- DMA continuous conversion for seamless data transfer
- Two filters with configurable filter coefficient
- Threshold monitoring which helps to trigger an interrupt

---

**Footer:**
Espressif Systems  
Page 57 ESP32-C6 Series Datasheet v1.4  

[Submit Documentation Feedback](#)