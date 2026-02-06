**Title: Peripherals**

---

### Pin Assignment

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

#### **5.2.1.7 LED PWM Controller**

The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller:

- Can generate digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 14 bits.
- Has multiple clock sources, including APB clock and external main crystal clock.
- Can operate when the CPU is in Light-sleep mode.
- Supports gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator.

---

### Pin Assignment

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

#### **5.2.1.8 Remote Control Peripheral**

The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols. All four channels share a 192 × 32-bit memory block to store transmit or receive waveform.

---

### Pin Assignment

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

#### **5.2.2 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.

##### 5.2.2.1 SAR ADC

ESP8685 integrates two 12-bit SAR ADCs:

- ADC1 supports measurements on 5 channels, and is factory-calibrated.
- ADC2 supports measurements on 1 channel, and is not factory-calibrated.

**Note:**
ADC2 of some chip revisions is not operable. For details, please refer to [ESP32-C3 Series SoC Errata](#).

---

### Pin Assignment

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#). 

---

*Espressif Systems*
*Submit Documentation Feedback*

**ESP8685-WROOM-03 Datasheet v1.5**