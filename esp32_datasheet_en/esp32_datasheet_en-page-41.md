**Title: Functional Description**

---

### Feature List

- **Three PWM timers for precise timing and frequency control**
  - Every PWM timer has a dedicated 8-bit clock prescaler
  
- The 16-bit counter in the PWM timer can work in count-up mode, count-down mode, or count-up-down mode
  
- A hardware sync can trigger a reload on the PWM timer with a phase register. It will also trigger the prescaler’ restart, so that the timer’s clock can also be synced, with selectable hardware synchronization source

- **Three PWM operators for generating waveform pairs**
  - Six PWM outputs to operate in several topologies
  
  - Configurable dead time on rising and falling edges; each set up independently
  
  - Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer

- **Fault Detection module**
  - Programmable fault handling in both cycle-by-cycle mode and one-shot mode
  
  - A fault condition can force the PWM output to either high or low logic levels

- Capture module for hardware-based signal processing
  - Speed measurement of rotating machinery
  
  - Measurement of elapsed time between position sensor pulses
  
  - Period and duty cycle measurement of pulse train signals
  
  - Decoding current or voltage amplitude derived from duty-cycle-encoded signals of current/voltage sensors
  
  - Three individual capture channels, each of which with a 32-bit time-stamp register
  
  - Selection of edge polarity and prescaling of input capture signals
  
  - The capture timer can sync with a PWM timer or external signals

For details, see [ESP32 Technical Reference Manual](#) > Chapter Motor Control PWM.

---

### Pin Assignment

The pins for the Motor Control PWM can be chosen from any GPIOs via the GPIO Matrix. 

For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

**Subtitle: SD/SDIO/MMC Host Controller**

An SD/SDIO/MMC host controller is available on ESP32.
  
---

*Footer:* Espressif Systems, Submit Documentation Feedback, ESP32 Series Datasheet v5.2