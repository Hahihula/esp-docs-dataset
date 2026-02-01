**Title: Functional Description**

- **PWM duty cycle dithering**
- Automatic duty cycle fading
  - Linear duty cycle fading — only one duty cycle range
  - Gamma curve fading — up to 16 duty cycle ranges for each PWM generator, with independently configured fading direction (increase or decrease), fading amount, number of fades, and fading frequency

- **PWM signal output in low-power mode (Light-sleep mode)**
- Event generation and task response achieved by the Event Task Matrix (ETM)

For details, see [ESP32-H2 Technical Reference Manual](#) > Chapter LED PWM Controller.

**Subtitle: Pin Assignment**

The pins for the LED PWM Controller can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

**Title: Motor Control PWM (4.2.1.9)**

The Motor Control Pulse Width Modulator (MCPWM) is designed for driving digital motors and smart light. The MCPWM is divided into five main modules: PWM timers, PWM operators, Capture module, Fault Detection module, and Event Task Matrix (ETM) module.

**Subtitle: Feature List**

- Three PWM timers for precise timing and frequency control
  - Every PWM timer has a dedicated 8-bit clock prescaler
  - The 16-bit counter in the PWM timer can work in count-up mode, count-down mode, or count-up-down mode

- Hardware or software synchronization to trigger a reload on the PWM timer or the prescaler’s restart with selectable hardware synchronization source

- Three PWM operators for generating waveform pairs
  - Six PWM outputs to operate in several topologies
  - The control of the PWM signal can be updated asynchronously
  - Configurable dead time on rising and falling edges; each set up independently
  - Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer

- Period, time stamps, and important control registers have shadow registers with flexible updating methods

- Capture module for hardware-based signal processing
  - Speed measurement of rotating machinery

**Footer:**
Espressif Systems  
45  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2