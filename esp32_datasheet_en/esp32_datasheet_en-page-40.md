**Title: Functional Description**

---

### Feature List

- Eight independent pulse counter units
- Each pulse counter unit has a 16-bit signed counter register and two channels
- Counter modes: increment, decrement, or disable
- Glitch filtering for input pulse signals and control signals
- Selection between counting on rising or falling edges of the input pulse signal

For details, see [ESP32 Technical Reference Manual](#) > Chapter Pulse Count Controller.

---

### Pin Assignment

The pins for the Pulse Count Controller can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

#### Subsection: LED PWM Controller (Section 4.8.8)

**Title:** LED PWM Controller

The LED PWM Controller (LEDC) is designed to generate PWM signals for LED control.

### Feature List

- Sixteen independent PWM generators
- Maximum PWM duty cycle resolution of 20 bits
- Eight independent timers with 20-bit counters, configurable fractional clock dividers and counter overflow values
- Adjustable phase of PWM signal output
- PWM duty cycle dithering
- Automatic duty cycle fading

For details, see [ESP32 Technical Reference Manual](#) > Chapter LED PWM Controller.

---

### Pin Assignment

The pins for the LED PWM Controller can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

#### Subsection: Motor Control PWM (Section 4.8.9)

**Title:** Motor Control PWM

The Pulse Width Modulation (PWM) controller can be used for driving digital motors and smart lights. The controller consists of PWM timers, the PWM operator and a dedicated capture sub-module. Each timer provides timing in synchronous or independent form, and each PWM operator generates a waveform for one PWM channel. The dedicated capture sub-module can accurately capture events with external timing.

---

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

[Submit Documentation Feedback](#)