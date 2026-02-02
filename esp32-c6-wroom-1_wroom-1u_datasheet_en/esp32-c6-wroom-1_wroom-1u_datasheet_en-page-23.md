**Title: Peripherals**

- **Hardware synchronization**: Hardware or software synchronization to trigger a reload on the PWM timer or the prescaler's restart, with selectable hardware synchronization source.
  
  - Three PWM operators for generating waveform pairs
  
    - Six PWM outputs operate in several topologies
  
    - Configurable dead time on rising and falling edges; each set up independently
  
    - Modulating of PWM output by high-frequency carrier signals, useful when gate drivers are insulated with a transformer
  
- **Capture module**: Capture module for hardware-based signal processing
  
  - Speed measurement of rotating machinery
  
  - Measurement of elapsed time between position sensor pulses
  
  - Period and duty cycle measurement of pulse train signals
  
  - Decoding current or voltage amplitude derived from duty-cycle-encoded signals of current/voltage sensors
  
  - Three individual capture channels, each with a 32-bit time-stamp register
  
  - Selection of edge polarity and prescaling of input capture signals
  
  - The capture timer can sync with a PWM timer or external signals

- **Fault Detection module**: Fault detection module
  
  - Programmable fault handling in both cycle-by-cycle mode and one-shot mode
  
  - A fault condition can force the PWM output to either high or low logic levels
  
  - Event generation and task response achieved by the Event Task Matrix (ETM)

**Subtitle: Pin Assignment**

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment.

**Title: Remote Control Peripheral**
  
- **5.2.1.11**: The title is "Remote Control Peripheral".

  - Four channels for sending and receiving infrared remote control signals
  
  - Independent transmission and reception capabilities for each channel
  
  - Support for Normal TX/RX mode, Wrap TX/RX mode, Continuous TX mode
  
  - Modulation on TX pulses and Demodulation on RX pulses
  
  - RX filtering for improved signal reception
  
  - Ability to transmit data simultaneously on multiple channels
  
  - Clock divider counter, state machine, and receiver for each RX channel

**Footer**: Espressif Systems  
Page number: 23  
Document version: ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4  

[Submit Documentation Feedback](#)