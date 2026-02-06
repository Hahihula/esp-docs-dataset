**Title: Peripherals**

- **64-byte receive FIFO**
  - Acceptance filter (single and dual filter modes)
  - Error detection and handling: error counters, configurable error interrupt threshold, error code capture, arbitration lost capture

For details, see [ESP32-C3 Technical Reference Manual > Chapter Two-wire Automotive Interface](#).

---

**Pin Assignment**

- **5.2.1.7 LED PWM Controller**
  For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).
  
  The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller:
  - Can generate digital waveform with configurable periods and duty cycle.
    *The resolution of duty cycle can be up to 14 bits.*
  - Has multiple clock sources, including APB clock and external main crystal clock.
  - Can operate when the CPU is in Light-sleep mode.
  - Supports gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator.

For details, see [ESP32-C3 Technical Reference Manual > Chapter LED PWM Controller](#).

---

**Pin Assignment**

- **5.2.1.8 Remote Control Peripheral**
  
  The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols. All four channels share a 192 x 32-bit memory block to store transmit or receive waveform.

For more details, see [ESP32-C3 Technical Reference Manual > Chapter Remote Control Peripheral (RMT)](#).

---

**Pin Assignment**

- **5.2.2 Analog Signal Processing**
  
  This subsection describes components on the chip that sense and process real-world data.
  
  For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).