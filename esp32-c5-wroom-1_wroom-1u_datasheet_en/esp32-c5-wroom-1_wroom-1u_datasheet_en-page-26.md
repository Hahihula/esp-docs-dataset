Title: Peripherals

- operation when the CPU is in Light-sleep mode
- gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator
- up to 16 duty cycle ranges for gamma curve generation, each can be independently configured in terms of duty cycle direction (increase or decrease), step size, the number of steps, and step frequency

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter LED PWM Controller.

---

Title: Pin Assignment

Body Text:
The pins for the LED PWM controller can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

---

Subtitle: 5.2.1.8 Pulse Count Controller

Body Text:
The Pulse Count controller (PCNT) in ESP32-C5 captures pulses and counts pulse edges in seven modes.
For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Pulse Count Controller.

#### Feature List
- four independent pulse counters (units) that count from 1 to 65535
- each unit consists of two independent channels sharing one pulse counter
- all channels have input pulse signals (e.g., sig_ch0_un) with their corresponding control signals (e.g., ctrl_ch0_un)
- independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit
- each channel has the following parameters:
  - selection between counting on positive or negative edges of the input pulse signal
  - configuration to Increment, Decrement, or Disable counter mode for control of signal’s high and low states
  - support step counting
  - maximum frequency of pulses: 40 MHz

---

Subtitle: Pin Assignment

Body Text:
The pins for the Pulse Count controller can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

---

Subtitle: 5.2.1.9 Motor Control PWM

Body Text:
ESP32-C5 integrates an MCPWM that can be used to drive digital motors and smart light.
Espressif Systems
Page Number: 26
Document Title: ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8 PRELIMINARY

[Submit Documentation Feedback](#)