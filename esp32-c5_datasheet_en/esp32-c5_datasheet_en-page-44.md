**Title: Functional Description**

- **stack pointer (SP) monitoring:** Prevent stack overflow or erroneous push/pop operations violation will trigger an interrupt.
- **program counter (PC) logging:** Record PC value. The developer can get the last PC value at the most recent CPU reset
- **bus access logging:** Record information about bus access when the CPU or DMA writes a specified value

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Debug Assistant (ASSIST_DEBUG).

---

**Subtitle: 4.1.3.14 Brownout Detector**

ESP32-C5 can periodically monitor the voltage of the power supply, and in the event of abnormal voltage, it is capable of generating interrupts or initiating resets.

- **Feature List**
  - configurable detection threshold
  - configurable reset level
  - glitch filtering

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Power Supply Detector.

---

**Subtitle: 4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

- **4.1.4.1 AES Accelerator**
  - ESP32-C5 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software.
  - The AES accelerator integrated in ESP32-C5 has two working modes, which are typical AES and DMA-AES.

- **Feature List**
  - typical AES working mode
    - AES-128/AES-256 encryption and decryption, compliant with [NIST FIPS 197](#)
  - DMA-AES working mode
    - AES-128/AES-256 encryption and decryption, compliant with [NIST FIPS 197](#)
  - block cipher mode, compliant with NIST SP 800-38A

*ECB (Electronic Codebook)*  
*CBC (Cipher Block Chaining)*  
*OFB (Output Feedback)*  
*CTR (Counter)*

---

**Footer:**
Espressif Systems
44 Submit Documentation Feedback ESP32-C5 Series Datasheet v1.0