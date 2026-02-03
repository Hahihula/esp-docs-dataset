- **2 cores at 240 MHz: 1079.96 CoreMark; 4.50 CoreMark/MHz**

**448 KB ROM**
**520 KB SRAM**
**16 KB SRAM in RTC**
**QSPI supports multiple flash/SRAM chips**

### Clocks and Timers
- Internal 8 MHz oscillator with calibration
- Internal RC oscillator with calibration
- External 2 MHz ~ 60 MHz crystal oscillator (40 MHz only for Wi-Fi/Bluetooth functionality)
- External 32 kHz crystal oscillator for RTC with calibration

- Two timer groups, including 2 × 64-bit timers and 1 × main watchdog in each group
- One RTC timer
- RTC watchdog

### Advanced Peripheral Interfaces
- **34 programmable GPIOs**
  - Five strapping GPIOs
  - Six input-only GPIOs
  - Six GPIOs needed for in-package flash (ESP32-U4WDH) and in-package PSRAM (ESP32-D0WDRH2-V3)
- 12-bit SAR ADC up to 18 channels
- Two 8-bit DAC
- Ten touch sensors
- Four SPI interfaces
- Two I2S interfaces
- Two I2C interfaces
- Three UART interfaces
- One host (SD/eMMC/SDIO)
- One slave (SDIO/SPI)
- Pulse count controller
- Ethernet MAC interface with dedicated DMA and IEEE 1588 support
- TWAI®, compatible with ISO 11898-1 (CAN Specification 2.0)
- RMT (TX/RX)

Espressif Systems  
Submit Documentation Feedback ESP32 Series Datasheet v5.2