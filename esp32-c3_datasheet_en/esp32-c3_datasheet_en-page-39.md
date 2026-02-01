**Title: Functional Description**

---

### ESPressif's ESP32-C3 Wi-Fi + Bluetooth Low Energy SoC

#### Digital Power Domain

- **CPU**
  - RISC-V 32-bit Microprocessor
  - JTAG
  - I2C
  - GPIO
  - TWAI® (General-purpose Timers)
  - Cache
  - SPI0/1
  - I2S
  - UART
  - USB Serial/UTAG

- **World Controller**
  - Debug Assistant
  - RNG
  - LED PWM
  - Flash Encryption
  - Main System Watchdog Timers

- **ROM**
  - SRAM
  - DIG ADC
  - RMT
  - Temperature Sensor
  - System Timer

#### Wireless Digital Circuits

- Bluetooth LE Link Controller: Wi-Fi MAC, SHA, RSA, HMAC, Digital Signature
- Bluetooth LE Baseband: Wi-Fi AES, SPI2, Secure Boot, GDMA
- Baseband:

#### Optional Digital Peripherals

- 

#### Analog Power Domain

- **RTC Power Domain**
  - PMU (Power Management Unit)
  - eFuse Controller
  - Brownout Detector
  - RTC Memory
  - Super Watchdog Timer
  
- **RF Circuits**
  - 2.4 GHz Receiver, Transmitter, Synthesizer + Switch
  - PLL: Phase Lock Loop

#### Power Distribution:

- Power domain (Power subdomain)

---

**Figure Caption:** Figure 4-2. Components and Power Domains.

---

### Table Title: Table 4-1. Components and Power Domains

| Mode | RTC | Digital | Analog | Optional Wireless Peripherals |
|------|-----|---------|--------|--------------------------------|
| Active | ON   | ON      | ON     | ON                             |
| Modem-sleep | ON    | ON      | ON     | OFF                            |
| Light-sleep  | ON    | OFF     | ON     | OFF                            |
| Deep-sleep   | ON    | OFF     | ON     | OFF                            |

1. Configurable, see the TRM.
2. If Wireless Digital Circuits are on, RF circuits are periodically switched on when required by internal operation to keep active wireless connections running.

---

**For details:** ESP32-C3 Technical Reference Manual > Chapter Low-Power Management (RTC_CNTL).

---

Espressif Systems  
Page 39  
ESP32-C3 Series Datasheet v2.2  

[Submit Documentation Feedback](#)