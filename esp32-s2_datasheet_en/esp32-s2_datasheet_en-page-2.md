**Title:**
Product Overview

**Body Text:**
ESP32-S2 is a highly-integrated low-power MCU-based system on a chip (SoC) with 2.4 GHz Wi-Fi. It consists of a single-core microprocessor (Xtensa® 32-bit LX7), an ultra-low-power coprocessor, a Wi-Fi baseband, RF module, and numerous peripherals.

The functional block diagram of the SoC is shown below:

**Block Diagram:**
- **Espressif’s ESP32-S2 Wi-Fi SoC**

  - **Core System:** 
    - Xtensa® Single-Core
      - 32-bit LX7 Microprocessor

  - **Wireless MAC and Baseband:** 
    - Wi-Fi MAC
    - Wi-Fi Baseband

  - **RF:**
    - 2.4 GHz Balun + Switch
    - 2.4 GHz Transmitter
    - RF Synthesizer
    - 2.4 GHz Receiver

  - **Cache:** SRAM, ROM

  - **JTAG**

- **Peripherals (with specific power modes):**
  - SPI0/1: Active and Modem-sleep; option in Light-sleep mode.
  - I2C: Active
  - GPIO: Active, Modem-sleep, and Light-sleep;
  - SPI2/3: Active, Modem-sleep, Light-sleep,
  - I2S: Active (all modes)
  - UART: Active; option in Light-sleep mode.
  - Touch Sensor:
    - Temperature Sensor
    - Pulse Counter

- **RTC:** 
  - RTC GPIO Memory Brownout Detector
  
- **Security:**
  - SHA, RSA, AES, RNG,
  - eFuse Controller (all modes)
  - RTC Watchdog Timer; option in Light-sleep mode.
  - HMAC Digital Signature Secure Boot Flash Encryption
  - System Timer
  - USB OTG

**Footer Text:**
For more information on power consumption, see Section 4.13.3 Power Management Unit.

**Document Information:** 
- ESP32-S2 Functional Block Diagram
- For reference in the datasheet v1.8 Series Datasheet of ESP32-S2.
- Page number and footer text: "Submit Documentation Feedback"