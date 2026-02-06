**Title: Peripherals**

---

### Feature List

- Can generate a digital waveform with configurable periods and duty cycle. The duty cycle resolution can be up to 14 bits within a 1 ms period.
- Multiple clock sources, including APB clock and external main crystal clock.
- Can operate when the CPU is in Light-sleep mode
- Gradual increase or decrease of duty cycle, useful for the LED RGB color-fading generator

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter LED PWM Controller.

---

### Pin Assignment

For LED PWM, the pins used can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and [ESP32-S3 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

---

#### 5.2.1.11 Motor Control PWM (MCPWM)

ESP32-S3 integrates two MCPWs that can be used to drive digital motors and smart light. Each MCPWM peripheral has one clock divider (prescaler), three PWM timers, three PWM operators, and a capture module. PWM timers are used for generating timing references. The PWM operators generate desired waveform based on the timing references. Any PWM operator can be configured to use the timing references of any PWM timers. Different PWM operators can share the same PWM timer’s timing reference signals.

PWM operators also have different PWM timers’ values to produce the PWM signals that work alone, and some PWM timers are synchronized together.
For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter Motor Control PWM.

---

#### 5.2.1.12 Remote Control Peripheral (RMT)

The Remote Control Peripheral is designed for sending and receiving infrared remote control signals:

- Four TX channels
- Four RX channels
- Support multiple channels (programmable) transmitting data simultaneously.
- Eight channels share a 384 x 32-bit RAM

Support modulation on TX pulses.

Support filtering and demodulation on RX pulses. 

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#)

ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6