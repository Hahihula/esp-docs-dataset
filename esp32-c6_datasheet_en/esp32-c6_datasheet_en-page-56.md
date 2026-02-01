**Title: Functional Description**

- Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer

**Subtitle: Capture module for hardware-based signal processing**
  - Speed measurement of rotating machinery
  - Measurement of elapsed time between position sensor pulses
  - Period and duty cycle measurement of pulse train signals
  - Decoding current or voltage amplitude derived from duty-cycle-encoded signals of current/voltage sensors
  - Three individual capture channels, each of which with a 32-bit time-stamp register
  - Selection of edge polarity and prescaling of input capture signals
  - The capture timer can sync with a PWM timer or external signals

**Subtitle: Fault Detection module**
  - Programmable fault handling in both cycle-by-cycle mode and one-shot mode
  - A fault condition can force the PWM output to either high or low logic levels

**Subtitle: Event generation and task response achieved by the Event Task Matrix (ETM)**

For details, see [ESP32-C6 Technical Reference Manual](#) > Chapter Motor Control PWM (MCPWM).

---

**Title: Pin Assignment**

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

**Subtitle: Remote Control Peripheral**
4.2.1.11
The Remote Control Peripheral (RMT) controls the transmission and reception of infrared remote control signals.
- Four channels for sending and receiving infrared remote control signals
- Independent transmission and reception capabilities for each channel
- Support for Normal TX/RX mode, Wrap TX/RX mode, Continuous TX mode
- Modulation on TX pulses and Demodulation on RX pulses
- RX filtering for improved signal reception
- Ability to transmit data simultaneously on multiple channels
- Clock divider counter, state machine, and receiver for each RX channel
- Default allocation of RAM blocks to channels based on channel number
- RAM containing 16-bit entries with “level” and “period” fields

For more details, see [ESP32-C6 Technical Reference Manual](#) > Chapter Remote Control Peripheral (RMT).

---

**Footer:**
Espressif Systems  
56  
[Submit Documentation Feedback](#)  
ESP32-C6 Series Datasheet v1.4