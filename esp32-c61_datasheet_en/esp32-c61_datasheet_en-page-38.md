**Title: Functional Description**

---

### Figure Caption:
- **Figure 4-2:** Components and Power Domains

#### Diagram Breakdown:

1. **Espressif's ESP32-C61 Wi-Fi + Bluetooth Low Energy SoC**
   - CPU (HP Power Domain)
     - RISC-V 32-bit Microprocessor
     - I2C, JTAG, System Timer, GPIO, Cache, Temperature Sensor, ROM, XTS-AES, LED PWM, Secure Boot

   - Memory:
     - SRAM: General-purpose SPI Timers
     - MMU (Main System Watchdog Timers)

   - Wireless Digital Circuits and Wi-Fi Link Controller:
     - Bluetooth LE Baseband, Wi-Fi MAC Modem Power, Brown-out Detector
   
   - **LP Power Domain**
     - LP IO PMU Super Watchdog TRNG

   - Analog Power Domain
     - RF Circuits: 2.4 GHz Receiver Transmitter, 2.4 GHz Balun Synthesizer + Switch

   - PLL RC_FAST_CLK XTAL_CLK Phase-Locked Loop Fast RC Oscillator External Main Clock

### Table Caption:
- **Figure 4-3:** Components and Power Domains Table

#### Table Breakdown:

| Mode | LP Power Domain Memory Wireless Pwr Circuits CPU Wireless Digital Curcuits Others RF Circuits |
|------|--------------------------------------------------|
| Active | ON | ON | ON | ON | ON |
| Modem_sleep | ON | ON | ON | ON | OFF |
| Light_sleep | ON | ON | OFF | OFF | OFF |
| Deep_sleep | ON | OFF | OFF | OFF | OFF |

#### Power Distribution:
- **Power Domain**
  - LP Power Domain
    - Always-on, LP Peri Memory Wireless Pwr Circuits CPU Wireless Digital Curcuits Others RF Circuits

- **Power Subdomain**

---

**Footer: Espressif Systems ESP32-C61 Series Datasheet v0.5 Page 38**