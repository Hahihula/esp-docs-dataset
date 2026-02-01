- Event task matrix (ETM)

## Analog interfaces:
- 12-bit SAR ADC, up to 4 channels
- Temperature sensor
- Brown-out detector
- Analog voltage comparator

## Timers:
- Two 54-bit general-purpose timers
- 52-bit system timer
- Two main system watchdog timers
- Three watchdog timers

### Power Management
- Fine-resolution power control through a selection of clock frequency, duty cycle, Wi-Fi operating modes, and individual power control of internal components
- Four power modes designed for typical scenarios: Active, Modem-sleep, Light-sleep, Deep-sleep
- Power consumption in Deep-sleep mode is 10 μA

### Security
- Secure boot - permission control on accessing internal and external memory
- Flash and PSRAM encryption - external memory encryption and decryption
- 4096-bit OTP, up to 1792 bits for users
- Cryptographic hardware acceleration:
  - Hash (FIPS PUB 180-4)
  - ECC (Curve P-192 and curve P-256 defined in FIPS 186-3 are supported)
  - Elliptic curve digital signature algorithm (ECDSA)
- True random number generator (TRNG)
- Power glitch detector

### RF Module
- Antenna switches, RF balun, power amplifier, low-noise receive amplifier
- Up to +19.5 dBm of power for an 802.11ax transmission
- Up to +21 dBm of power for an 802.11b transmission
- Up to –106 dBm receiver sensitivity for Bluetooth LE (125 Kbps)

Espressif Systems  
ESP32-C61 Series Datasheet v0.5

Page number: 5