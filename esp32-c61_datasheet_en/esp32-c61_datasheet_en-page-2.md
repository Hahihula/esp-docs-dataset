Title: Product Overview

Body Text:
ESP32-C61 is a low-power MCU-based system on chip (SoC). ESP32-C61 integrates 2.4 GHz Wi-Fi 6 and Bluetooth® Low Energy (Bluetooth LE). ESP32-C61 consists of a 32-bit RISC-V single-core microprocessor, a Wi-Fi baseband, a Bluetooth LE baseband, RF module, and numerous peripherals.

The functional block diagram of the SoC is shown below:

Functional Block Diagram:
- **Espressif's ESP32-C61 Wi-Fi + Bluetooth® Low Energy SoC**
  - CPU System
    - RISC-V 32-bit Microprocessor (SRAM)
    - ROM, JTAG
  - Wireless MAC and Baseband
    - Wi-Fi Baseband: Bluetooth LE Baseband; Wi-Fi MAC Link Controller
  - RF:
    - 2.4 GHz Balun + Switch
    - 2.4 GHz Transmitter
    - 2.4 GHz Receiver
    - RF Synthesizer

- **Peripherals**
  - I2C, I2S, ETM; LP IO (PMU)
  - GPIO: LED PWM USB Serial/JTAG eFuse Controller
  - UART GDMA Super Watchdog TRNG ECC
  - ADC System Timer RTC Watchdog Timer Secure Boot
  - SDIO 2.0 Slave Temperature Sensor Brown-out Detector Digital Signature - ECDSA

- **Power Management**
  - SHA APM (optional in Light-sleep)
  - Flash/PSRAM Encryption XTS-AES Power Glitch Detector
  
- Modules having power in specific power modes:
  - Active
  - Active and Modem-sleep: optional in Deep-sleep All modes

Caption under diagram:
ESP32-C61 Functional Block Diagram

Footer Text:
For more information on power consumption, see Section **4.1.3.7 Power Management Unit**.

Company Information at the bottom of page:
Espressif Systems
Page number and document reference: ESP32-C61 Series Datasheet v0.5