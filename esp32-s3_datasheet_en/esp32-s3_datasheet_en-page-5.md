- RMT (TX/RX)
- Pulse count controller

### Analog signal processing:
- Two 12-bit SAR ADCs, up to 20 channels
- Temperature sensor
- 14 capacitive touch sensing IOs

### Timers:
- Four 54-bit general-purpose timers
- 52-bit system timer
- Three watchdog timers

### Power Management
- Fine-resolution power control, including clock frequency, duty cycle, Wi-Fi operating modes, and individual internal component control
- Four power modes designed for typical scenarios: Active, Modem-sleep, Light-sleep, Deep-sleep
- Power consumption in Deep-sleep mode is 7 μA
- RTC memory remains powered on in Deep-sleep mode

### Security
- Secure boot - permission control on accessing internal and external memory
- Flash encryption - memory encryption and decryption
- Cryptographic hardware acceleration:
  - AES-128/256 (FIPS PUB 197)
  - SHA (FIPS PUB 180-4)
  - RSA
  - Random Number Generator (RNG)
  - HMAC
  - Digital signature

### RF Module
- Antenna switches, RF balun, power amplifier, low-noise receive amplifier
- Up to +21 dBm of power for an 802.11b transmission
- Up to +19.5 dBm of power for an 802.11n transmission
- Up to -104.5 dBm of sensitivity for Bluetooth LE receiver (125 Kbps)

Espressif Systems  
ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)