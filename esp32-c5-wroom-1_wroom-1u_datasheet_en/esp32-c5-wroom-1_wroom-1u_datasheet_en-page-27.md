**Title: Peripherals**

---

### Feature List

- a clock divider (prescaler), three PWM timers, three PWM operators, and a dedicated capture submodule. PWM timers are used to generate timing references. PWM operators generate desired waveform based on the timing references.
- a PWM operator can use the timing reference of any PWM timer
- a PWM operator can use the same timing reference with other PWM operators
- PWM operators can use different PWM timers’ values to produce independent PWM signals
- PWM timers can be synchronized

For details, see [ESP32-C5 Technical Reference Manual](https://www.espressif.com/sites/default/files/documentation/esp32-c5_technical_reference_manual.pdf) > Chapter Motor Control PWM (MCPWM).

---

### Pin Assignment

The pins for the Motor Control PWM can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-c5_datasheet.pdf) > Section IO Pins and [ESP32-C5 Technical Reference Manual](https://www.espressif.com/sites/default/files/documentation/esp32-c5_technical_reference_manual.pdf) > Chapter GPIO Matrix and IO MUX.

---

**Title: 5.2.10 Remote Control Peripheral**

The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols.

### Feature List

- four channels:
  - TX channels 0 ~ 1
  - RX channels 2 ~ 3
- the transmitter supports:
  - normal TX mode
  - wrap TX mode
  - modulation on TX pulses
  - continuous TX mode
- multiple channels (programmable) transmitting data simultaneously

### The receiver supports:

- normal RX mode
- wrap RX mode
- RX filtering
- demodulation on RX pulses

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](https://www.espressif.com/contact-us)  
ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8 PRELIMINARY