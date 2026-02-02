**Title: Peripherals**

- **Sampling frequencies can be**: 
  - 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz,
  - etc.
  
- **8-/16-/24-/32-bit data communication**
  
- **Direct Memory Access (DMA)**
  
- **A-law and μ-law compression/decompression algorithms for improved signal-to-quantization noise ratio**
  
- **Flexible data format control**

**Subtitle: Pin Assignment**

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment

---

**Title: 5.2.1.5 Pulse Count Controller**

The Pulse Count Controller (PCNT) is designed to count input pulses by tracking rising and falling edges of the input pulse signal.

**Subtitle: Feature List**
  
- Four independent pulse counters with two channels each
- Counter modes: increment, decrement, or disable
- Glitch filtering for input pulse signals and control signals
- Selection between counting on rising or falling edges of the input pulse signal

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment

---

**Title: 5.2.1.6 USB Serial/JTAG Controller**

The USB Serial/JTAG controller in the ESP32-C6 chip provides an integrated solution for communicating to the chip over a standard USB CDC-ACM serial port as well as a convenient method for JTAG debugging. It eliminates the need for external chips or JTAG adapters, saving space and reducing cost.

**Subtitle: Feature List**
  
- **USB 2.0 full speed compliant**, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
- **CDC-ACM**:
  - CDC-ACM adherent serial port emulation (plug-and-play on most modern OSes)
  - Host controllable chip reset and entry into download mode
  
- **JTAG adapter functionality**: 
  - Fast communication with CPU debugging core using a compact representation of JTAG instructions

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment

---

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4