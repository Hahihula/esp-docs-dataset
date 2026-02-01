**Title:**
Product Overview

**Body Text:**
ESP32-H2 is a low-power MCU-based system on a chip (SoC) with integrated 2.4 GHz Bluetooth® Low Energy (Bluetooth LE) and 802.15.4. It consists of an RISC-V 32-bit microprocessor, a Bluetooth LE baseband, an 802.15.4 baseband, RF module, and numerous peripherals.

The functional block diagram of the SoC is shown below:

**Block Diagram:**
- **CPU and Memory:** 
  - CPU
    - RISC-V 32-bit Microprocessor (with a note indicating "Switch")
    - Cache
      - SRAM
        - Fast RC Oscillator, Bluetooth LE Link Controller, Interrupt Matrix
    - JTAG ROM

- **RF:**
  - Switches for various RF components:
    - 802.15.4 MAC Baseband (with a note indicating "XTAL OSC")

- **Wireless Digital Circuits:** 
  - 32 MHz XTAL OSC
  - PLL, Bluetooth LE Baseband

- **Peripherals:**
  - GDMA System Timer General-purpose Timers
    - GPIO LP GPIO SHA RSA AES RNG
  - Event Task Matrix Pulse Counter PARLIO USB Serial/ JTAG RTC Secure Boot Flash Encryption
  - SPI0/1 SPI2 I2S Main System Watchdog RTC Permission Control ECC
  - UART TWAI® I2C Watchdog Timers TEE ECDSA

- **Security:**
  - eFuse Controller, HMAC Digital Signature (with a note indicating "eFuse Controller")

- **LP System:** 
  - Temperature Sensor Super Watchdog LP Memory PMU Analog PAD Voltage Comparator Brown-out Detector
  - RMT LED PWM MCPWM 

**Subtitle: Power consumption**

**Diagram Description under Subtitle:**
Brown–out Detector

**Footer Text:**
For more information on power consumption, see Section **4.1.3.6 Power Management Unit**.

**Document Footer Information:** 
Espressif Systems
2 ESP32-H2 Series Datasheet v1.2 Submit Documentation Feedback