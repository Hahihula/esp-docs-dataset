**Title: Functional Description**

---

### Pin Assignment

The pins for the LED PWM controller can be chosen from any GPIOs via the GPIO Matrix.

#### Section Title: **4.2.2.16 Motor Control PWM (MCPWM)**

ESP32-P4 integrates two MCPWMs that can be used to drive digital motors and smart light. Every MCPWM has a clock divider (prescaler), three PWM timers, three PWM operators, a dedicated capture submodule, an Event Task Matrix (ETM) module, and an fault detection module.

**Feature List**

PWM timers are used to generate timing references. The PWM operators generate desired waveform based on the timing references. By configuration, a PWM operator can use the timing reference of any PWM timer, and use the same timing reference with other PWM operators. PWM operators can also use different PWM timers’ values to produce independent PWM signals. PWM timers can be synchronized.

---

### Pin Assignment

The pins for the motor control PWM can be chosen from any GPIOs via the GPIO Matrix.

#### Section Title: **4.2.2.17 Remote Control Peripheral (RMT)**

The Remote Control Peripheral (RMT) supports four channels of infrared remote transmission and four channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols.

**Feature List**

- Eight channels:
  - TX channels 0–3
  - RX channels 4–7
- Eight channels share a 384 x 32-bit RAM

**The transmitter supports:**
- Normal TX mode
- Wrap TX mode
- Continuous TX mode
- Modulation on TX pulses
- Multiple channels transmitting data simultaneously (programmable)
- GDMA access supported by TX channel 3

**The receiver supports:**
- Normal RX mode
- Wrap RX mode

---

Espressif Systems  
74 ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)