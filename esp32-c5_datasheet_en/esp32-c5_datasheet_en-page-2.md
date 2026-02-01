Title: Product Overview

Body Text:
The ESP32-C5 SoC (System on Chip) supports 2.4 and 5 GHz dual-band Wi-Fi 6, Bluetooth LE 5, Zigbee 3.0 and Thread 1.4. It consists of a high-performance (HP) 32-bit RISC-V processor, an low-power (LP) 32-bit RISC-V processor, wireless baseband and MAC (Wi-Fi, Bluetooth LE, and 802.15.4), RF module, and numerous peripherals, with time-division coexistence of Wi-Fi, Bluetooth and 802.15.4.

The functional block diagram of the SoC is shown below:

[Functional Block Diagram]

Subtitles within Functional Block Diagram:
- CPU System
  - HP RISC-V: 32-bit Microprocessor
    - Cache
    - JTAG
  - LP RISC-V: 32-bit Microprocessor
    - HP Memory
    - ROM

- Wireless MAC and Baseband (Wi-Fi)
  - Wi-Fi Baseband
  - Bluetooth LE Baseband
  - 802.15.4 Baseband
  
- 2.4/5 GHz RF:
  - Balun + Switch: Transmitter, Receiver
  - Synthesizer

- Power Management Unit:

Peripherals (with various components listed):
- SPI
- I2C
- GPIO
- LP IO
- CAN FD
- I2S
- UART
- RTC Watchdog Timer
- GDMA
- PCNT
- RMT
- RTC Super Watchdog Timer
- LED PWM
- ETM
- ADC
- RTC Timer

Security:
- AES, SHA, RSA (with icons indicating active and optional modes)
- HMAC, ECC (with icon for digital signature)

Power Management Unit Functions: 
- Brownout Detector SDIO Slave Main System Watchdog Timers LP I2C eFuse Controller Secure Boot TEE Controller Flash/PSRAM Encryption (XTS-AES) Power Glitch Detector

Modules having power in specific modes:
- Active
- Active and Modem-sleep
- Active, Modem-sleep, Light-sleep: optional in Deep-sleep All nodes; optional in Deep-sleep
  
Footer Text:
For more information on power consumption, see Section 4.13.6 Power Management Unit.

Company Information at the bottom of page:

Espressif Systems

Page Number and Document Reference (at the very end):
2
ESP32-C5 Series Datasheet v1.0

Link to Submit Documentation Feedback: [Submit Documentation Feedback]