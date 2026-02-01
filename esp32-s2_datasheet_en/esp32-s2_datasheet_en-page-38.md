**Title: Functional Description**

- **Deep-sleep mode:** Only the RTC memory and RTC peripherals are powered on. Wi-Fi connection data are stored in the RTC memory. The ULP co-processor is functional.
  
- **Hibernation mode:** The internal 8-MHz oscillator and ULP co-processor are disabled. The RTC recovery memory is powered down. Only one RTC timer on the slow clock and certain RTC GPIOs are active. The RTC timer or the RTC GPIOs can wake up the chip from the Hibernation mode.

For power consumption in different power modes, please refer to Chapter 5.6 [Current Consumption](#).

For more information, please refer to ESP32-S2 Technical Reference Manual > Chapter Low-Power Management (RTC_CNTL).

---

**4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

**4.1.4.1 Cryptographic Hardware Accelerators**

ESP32-S2 is equipped with hardware accelerators of general algorithms, such as AES (FIPS PUB 197), ECB/CBC/CFB/CTR (NIST SP 800-38A), GCM (NIST SP 800-38D), SHA (FIPS PUB 180-4), and RSA, which support independent arithmetic, such as large-number multiplication and large-number modular multiplication. The maximum operation length for RSA and large-number modular multiplication is 4096 bits. The maximum operand length for large-number multiplication is 2048 bits.

**4.1.4.2 Physical Security Features**

- Transparent external flash and RAM encryption (AES-XTS) with software inaccessible key prevents unauthorized readout of user application code or data.
  
- Secure Boot feature uses a hardware root of trust to ensure only signed firmware (with RSA-PSS signature) can be booted.

- HMAC module can use a software inaccessible MAC key to generate SHA-HMAC signatures for identity verification, as well as other uses.

- Digital Signature module can use a software inaccessible secure key to generate MAC signatures for Identity Verification. 

---

**Footer:**
Espressif Systems
ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback](#)