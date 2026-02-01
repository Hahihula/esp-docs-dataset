Title: Product Overview

Body Text:
The ESP32-C6 SoC (System on Chip) supports Wi-Fi in 2.4 GHz band, Bluetooth 5, Zigbee 3.0 and Thread 1.3. It consists of a high-performance (HP) 32-bit RISC-V processor, an low-power (LP) 32-bit RISC-V processor, wireless baseband and MAC (Wi-Fi, Bluetooth LE, and 802.15.4), RF module, and numerous peripherals. Wi-Fi, Bluetooth and 802.15.4 coexist with each other and share the same antenna.

The functional block diagram of the SoC is shown below:

Functional Block Diagram:
- **Espressif’s ESP32-C6 Wi-Fi + Bluetooth® Low Energy + 802.15.4 SoC**
  - CPU System
    - HP RISC-V: 32-bit Microprocessor, 32-bit Microprocessor (Cache), JTAG, SRAM, LP Memory.
  - Wireless MAC and Baseband:
    - Wi-Fi Baseband,
    - Bluetooth LE Baseband,
    - 802.15.4 Baseband
  - RF: 
    - 2.4 GHz Balun + Switch,
    - 2.4 GHz Transmitter,  
    - 2.4 GHz Receiver.
- **Peripherals**
  - SPI, I2C, GPIO, TWAI®, I2S, UART, GDMA, PCNT, RMT, LED PWM, ETM, ADC
  - PARLIO,
  - SDIO 2.0 Slave,
  - Brownout Detector,
  - Temperature Sensor.
- **Power Management**
  - LP IO: Power Management Unit,
  - RTC Watchdog Timer (Super Watchdog),
  - LP UART:
  - AES, Digital Signature, HMAC
  - eFuse Controller,
  - RNG, Clock Glitch Filter,
  - Flash Encryption APM

**Security Modules having power in specific power modes:** 
- Active: All modules.
- Active and Modem-sleep (optional in Light-sleep): All nodes optional in Deep-sleep.

Subtitle: ESP32-C6 Functional Block Diagram
Hyperlink Text:
For more information on power consumption, see Section 4.1.3.7 Power Management Unit

Footer Information:
Espressif Systems  
Page Number and Document Reference: 
2 Submit Documentation Feedback  
ESP32-C6 Series Datasheet v1.4