**Title: Functional Description**

---

### Feature List

- four independent pulse counters (units) that count from 1 to 65535
- each unit consists of two independent channels sharing one pulse counter
- all channels have input pulse signals (e.g. sig_ch0_un) with their corresponding control signals (e.g. ctrl_ch0_un)
- independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit
  - each channel has the following parameters:
    1. selection between counting on positive or negative edges of the input pulse signal
    2. configuration to Increment, Decrement, or Disable counter mode for control of signal's high and low states
- support step counting

**For details, see ESP32-C5 Technical Reference Manual > Chapter Pulse Count Controller**

---

### Pin Assignment

The pins for the Pulse Count controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Title: Motor Control PWM**

ESP32-C5 integrates an MCPWM that can be used to drive digital motors and smart light.

### Feature List

- a clock divider (prescaler), three PWM timers, three PWM operators, and a dedicated capture submodule. PWM timers are used to generate timing references. PWM operators generate desired waveform based on the timing references
  - a PWM operator can use the timing reference of any PWM timer
  - a PWM operator can use the same timing reference with other PWM operators
- PWM operators can use different PWM timers’ values to produce independent PWM signals

**PWM timers can be synchronized**

For details, see ESP32-C5 Technical Reference Manual > Chapter Motor Control PWM (MCPWM).

### Pin Assignment

The pins for the Motor Control PWM can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Footer:**
Espressif Systems
Page number: 55

Submit Documentation Feedback