**Title: Peripherals**

- Support DMA for data transfer
- Support wake-up from sleep when connection is retained

---

**Subtitle: Pin Assignment**
For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

**Section Title: 5.2.1.9 LED PWM Controller**

The LED PWM Controller (LEDC) is designed to generate PWM signals for LED control.

**Feature List**
- Six independent PWM generators
- Maximum PWM duty cycle resolution of 20 bits
- Four independent timers with 20-bit counters, configurable fractional clock dividers and counter overflow values
- Adjustable phase of PWM signal output
- PWM duty cycle dithering
- Automatic duty cycle fading
  - Linear duty cycle fading — only one duty cycle range
  - Gamma curve fading – up to 16 duty cycle ranges for each PWM generator, with independently configured fading direction (increase or decrease), fading amount, number of fades, and fading frequency
- PWM signal output in low-power mode (Light-sleep mode)
- Event generation and task response achieved by the Event Task Matrix (ETM)

**Pin Assignment**
For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

**Section Title: 5.2.10 Motor Control PWM**

The Motor Control Pulse Width Modulator (MCPWM) is designed for driving digital motors and smart light. The MCPWM is divided into five main modules: PWM timers, PWM operators, Capture module, Fault Detection module, and Event Task Matrix (ETM) module.

**Feature List**
- Three PWM timers for precise timing and frequency control
  - Every PWM timer has a dedicated 8-bit clock prescaler
  - The 16-bit counter in the PWM timer can work in count-up mode, count-down mode, or count-up-down mode

---

**Footer:**
Espressif Systems  
Page number: 22  
Document version: ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4  

[Submit Documentation Feedback](#)