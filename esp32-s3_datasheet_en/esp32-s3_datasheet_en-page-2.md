**Title:**
Product Overview

**Body Text:**
ESP32-S3 is a low-power MCU-based system on a chip (SoC) with integrated 2.4 GHz Wi-Fi and Bluetooth® Low Energy (Bluetooth LE). It consists of high-performance dual-core microprocessor (Xtensa® 32-bit LX7), a ULP coprocessor, a Wi-Fi baseband, a Bluetooth LE baseband, RF module, and numerous peripherals.

The functional block diagram of the SoC is shown below:

**Block Diagram:**
- **CPU and Memory:** Xtensa Dual-core 32-bit LX7 Microprocessor
  - Cache SRAM
  - Interrupt Matrix

- **RF (Radio Frequency):**
  - 2.4 GHz Balun + Switch
    - External Main Clock Wi-Fi MAC Baseband Fast RC Oscillator Bluetooth LE Link Controller Phase Lock Loop
  - 2.4 GHz RF Transmitter/Receiver

- **Wireless Digital Circuits:**
  - Wi-Fi Baseband Security
    - SHA, RSA, AES, RNG
    - HMAC DIG ADC RTC ADC
    - Digital Signature eFuse Secure Boot Flash Encryption

- **Peripheral Functions:** 
  - GDMA System General-purpose Timers GPIO RTC GPIO
  - SD/MMC Host Pulse World Controller USB Serial/ JTAG Controller
  - SPI0/1 SPI2/3 I2S Main System Watchdog Timers RTC Watchdog Timer Control
  - USB OTG TWAI® I2C
  - UART LED PWM MCPWM Super Watchdog Touch Sensor RTC Memory PMU
  - RMT LCD Camera Interface RTC I2C Temperature Sensor ULP Coprocessor

**Subtitle:**
Power consumption

**Body Text under Subtitle:**
ESP32-S3 Functional Block Diagram

For more information on power consumption, see Section **4.1.3.5 Power Management Unit (PMU)**.

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 Series Datasheet v2.1