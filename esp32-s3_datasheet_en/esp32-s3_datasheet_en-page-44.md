**Title: Functional Description**

---

### Subtitle: Expressif's ESP32-S3 Wi-Fi + Bluetooth® Low Energy SoC

#### Digital Power Domain Components:
- **CPU**
  - Xtensa® Dual-core 32-bit LX7 Microprocessor
  - Cache
  - World Controller Matrix (WGM)
  - ROM
  - RAM
  - Interrupts Counter
  - Pulse Counter
  - LCD Interface
  - Main System Watchdog Timers

- **Digital Peripheral Devices**
  - SPI0/1, I2C, GPIO, TWA® System Timer
  - Camera Interface (I2S)
  - UART USB Serial/JTAG General-purpose Timers
  - Pulse Counter
  - LCD Interface
  - Main System Watchdog Timers

- **Wireless Digital Circuits**
  - Bluetooth LE Link Controller: SHA, RSA, HMAC, Digital Signature Host
  - Wi-Fi MAC (Wi-Fi Baseband)
  - AFS SPI2/3 Secure Boot GDMA USB OTG
  
#### Analog Power Domain Components:
- **RTC Power Domain**
  - PMU eFuse, RTC Memory Controller

- **Analog Circuits: RF Circuits**
  - 2.4 GHz Receiver
  - Super Watchdog ULP Coprocessor Synthesizer + Switch

- **Optional RTC Peripherals**
  - PLL, RC_FAST_CLK XTAL_CLK Phase Lock Loop Fast RC Oscillator External Main Clock Temperature Sensor Timer

#### Power Distribution:
- **Power Domains and Subdomains:**
  - Power domain
  - Power subdomain
  
---

### Figure Caption (Figure 4-2):
Components and Power Domains.

---

### Table Title (Table 4-1):
Components and Power Domains

| Mode | RTC | Digital | Analog |
|------|-----|---------|--------|
| Active | ON | ON | ON |
| Modern-sleep | ON | ON | ON |
| Light-sleep | ON | OFF | OFF |
| Deep-sleep | ON | OFF | OFF |

#### Notes:
1. Configurable.
2. If Wireless Digital Circuits are on, RF circuits are periodically switched on when required by internal operation to keep active wireless connections running.

---

### Footer Information (For details):
- See ESP32-S3 Technical Reference Manual > Chapter Low Power Management
- For more information: ESP32-S3 Series Datasheet v2.1

---

**Page Number:** 44  
**Footer Links:** Submit Documentation Feedback