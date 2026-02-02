**Chapter Title:**
Chapter 29

**Section Heading:**
Motor Control PWM (MCPWM)

**Subsection 1: Introduction**

The Motor Control Pulse Width Modulator (MCPWM) peripheral is intended for motor and power control. It provides six PWM outputs that can be set up to operate in several topologies. One common topology uses a pair of PWM outputs driving an H-bridge to control motor rotation speed and rotation direction.

The timing and control resources inside are allocated into two major types of submodules: PWM timers and PWM operators. Each PWM timer provides timing references that can either run freely or be synced to other timers or external sources. Each PWM operator has all necessary control resources to generate waveform pairs for one PWM channel. The MCPWM peripheral also contains a dedicated capture submodule that is used in systems where accurate timing of external events is important.

ESP32 contains two MCPWM peripherals: MCPWMO and MCPWM1. Their **control registers** are located in 4-KB memory blocks starting at memory locations 0x3FF5E000 and 0x3FF6C000 respectively.

**Subsection 2: Features**

Each MCPWM peripheral has one clock divider (prescaler), three PWM timers, three PWM operators, and a capture module. Figure **29.2-1** shows the submodules inside and the signals on the interface. PWM timers are used for generating timing references. The PWM operators generate desired waveform based on the timing references. Any PWM operator can be configured to use the timing references of any PWM timers. Different PWM operators can use the same PWM timer’s timing references to produce related PWM signals. PWM operators can also use different PWM timers’ values to produce the PWM signals that work alone. Different PWM timers can also be synced together.

**Footer:**
Espressif Systems
647 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:** GoBack