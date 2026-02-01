**Title: Functional Description**

For details, see the [ESP32-C5 Technical Reference Manual > Chapter Elliptic Curve Digital Signature Algorithm (ECDSA)](#).

---

### 4.1.4.8 External Memory Encryption and Decryption

The ESP32-C5 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard algorithm specified in [IEEE Std 1619-2007](#), providing security for users’ application code and data stored in the external memory (flash and PSRAM). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) to the off-package flash, and securely run data-sensitive applications in PSRAM.

**Feature List**
- general XTS-AES algorithm, compliant with [IEEE Std 1619-2007](#)
- software-based manual encryption
- high-speed auto encryption without software
- high-speed auto decryption without software
- encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode
- configurable counter measures against DPA attacks
- flash and PSRAM use their own separate keys

For more details, see the [ESP32-C5 Technical Reference Manual > Chapter External Memory Encryption and Decryption (XTS_AES)](#).

---

### 4.1.4.9 True Random Number Generator

The ESP32-C5 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

**Feature List**
- RNG entropy source
  - thermal noise from high-speed ADC or SAR ADC
  - an asynchronous clock mismatch

For more details, see the [ESP32-C5 Technical Reference Manual > Chapter Random Number Generator (RNG)](#).

---

### 4.1.4.10 Power Glitch Detector

ESP32-C5 can monitor the voltage of the power supply in real time. When a voltage glitch occurs, the chip will reset immediately to prevent power glitch attacks.

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C5 Series Datasheet v1.0  

Page 48