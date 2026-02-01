**Title: Functional Description**

---

### Pin Assignment

For details, see Section **2.3.6 Peripheral Pin Assignment**.

---

#### 4.2.1.8 Remote Control Peripheral

The infrared remote controller supports four channels of infrared remote transmission and reception. By programming the pulse waveform, it supports various infrared and other single wire protocols. Four channels share a 256 x 32-bit block of memory to store the transmitting or receiving waveform.

For more information, please refer to **ESP32-S2 Technical Reference Manual** > Chapter Remote Control Peripheral (RMT).

---

### Pin Assignment

For details, see Section **2.3.6 Peripheral Pin Assignment**.

---

#### 4.2.1.9 Pulse Count Controller

The pulse counter captures pulse and counts pulse edges through multiple modes. It has four channels, each of which captures four signals at a time. The four input signals include two pulse signals and two control signals.

For more information, please refer to **ESP32-S2 Technical Reference Manual** > Chapter Pulse Count Controller (PCNT).

---

### Pin Assignment

For details, see Section **2.3.6 Peripheral Pin Assignment**.

---

#### 4.2.1.10 LED PWM Controller

The LED PWM controller can generate eight independent channels. The LED PWM controller:

- can generate digital waveforms with configurable periods and duties. The accuracy of duty can be up to 18 bits within a 1 ms period.
- has multiple clock sources, including APB clock and external crystal clock.
- can operate when the CPU is in Light-sleep mode.
- supports gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator.

For more information, please refer to **ESP32-S2 Technical Reference Manual** > Chapter LED PWM Controller (LEDC).

---

### Pin Assignment

For details, see Section **2.3.6 Peripheral Pin Assignment**.

---

Espressif Systems  
43  
Submit Documentation Feedback  
ESP32-S2 Series Datasheet v1.8