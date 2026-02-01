**Title: Functional Description**

---

### **4.1.4 Cryptography and Security Component**

This subsection describes the security features incorporated into the chip, which safeguard data and operations.

#### 4.1.4.1 SHA Accelerator

ESP32-S3 integrates an SHA accelerator, which is a hardware device that speeds up SHA algorithm significantly.

**Feature List**
- All the hash algorithms introduced in [FIPS PUB 180-4 Spec](#).
  - SHA-1
  - SHA-224
  - SHA-256
  - SHA-384
  - SHA-512
  - SHA-512/224
  - SHA-512/256
  - SHA-512/t

- Two working modes
  - Typical SHA
    - DMA-SHA
  - interleaved function when working in Typical SHA working mode
  - Interrupt function when working in DMA-SHA working mode

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter SHA Accelerator.

---

### **4.1.4.2 AES Accelerator**

ESP32-S3 integrates an Advanced Encryption Standard (AES) Accelerator, which is a hardware device that speeds up AES algorithm significantly.

**Feature List**
- Typical AES working mode
  - AES-128/AES-256 encryption and decryption
- DMA-AES working mode
  - AES-128/AES-256 encryption and decryption
  - Block cipher mode
    * ECB (Electronic Codebook)

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#) ESP32-S3 Series Datasheet v2.1

Page number: **48**