Title: Functional Description

Subtitle: Feature List
- Secure Digital (SD) memory version 3.0 and version 3.01
- Secure Digital I/O (SDIO) version 3.0
- Consumer Electronics Advanced Transport Architecture (CE-ATA) version 1.1
- Multimedia Cards (MMC version 4.41, eMMC version 4.5 and version 4.5i)
- Up to 80 MHz clock output

Subtitle: Three data bus modes:
- 1-bit
- 4-bit (supports two SD/SDIO/MMC 4.41 cards, and one SD card operating at 1.8 V in 4-bit mode)
- 8-bit

For details, see ESP32-S3 Technical Reference Manual > Chapter SD/MMC Host Controller.

Subtitle: Pin Assignment
For details, see Section 2.3.5 Peripheral Pin Assignment.

Subtitle: Feature List
- Can generate a digital waveform with configurable periods and duty cycle. The duty cycle resolution can be up to 14 bits within a 1 ms period

- Multiple clock sources, including APB clock and external main crystal clock

- Can operate when the CPU is in Light-sleep mode

- Gradual increase or decrease of duty cycle, useful for the LED RGB color-fading generator

For details, see ESP32-S3 Technical Reference Manual > Chapter LED PWM Controller.

Subtitle: Pin Assignment
For details, see Section 2.3.5 Peripheral Pin Assignment.

Title: Motor Control PWM (MCPWM)

Subtitle: Description of MCPWM in ESP32-S3:
ESP32-S3 integrates two MCPWs that can be used to drive digital motors and smart light. Each MCPWM peripheral has one clock divider (prescaler), three PWM timers, three PWM operators, and a capture module. PWM timers are used for generating timing references. The PWM operators generate desired waveform based on the timing references. Any PWM operator can be configured to use the timing references of any PWM timers. Different PWM operators can use the same PWM timer’s timing references to produce related PWM signals. PWM operators can also use different PWM timers’ values to produce the PWM signals that work alone. Different PWM timers can also be synchronized together.

For details, see ESP32-S3 Technical Reference Manual > Chapter Motor Control PWM.

Footer:
Espressif Systems
57

Link: Submit Documentation Feedback

Document Title at Bottom Right Corner (partially visible): ESP32-S3 Series Datasheet v2.1