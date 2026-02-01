**Title: Functional Description**

---

### Feature List

- The following hash algorithms introduced in [FIPS PUB 180-4 Spec](#).
  - SHA-1
  - SHA-224
  - SHA-256

- Two working modes
  - Typical SHA
  - DMA-SHA

- Interleaved function when working in Typical SHA working mode
- Interrupt function when working in DMA-SHA working mode

For more details, see the [ESP32-C3 Technical Reference Manual > Chapter SHA Accelerator (SHA)](#).

---

### Section: Digital Signature 

#### Subsection 4.1.4.5 - Digital Signature

The Digital Signature (DS) module in the ESP32-C3 chip generates message signatures based on RSA with hardware acceleration.

- **Feature List**
  - RSA digital signatures with key length up to 3072 bits
  - Encrypted private key data, only decryptable by DS module
  - SHA-256 digest to protect private key data against tampering by an attacker

For more details, see the [ESP32-C3 Technical Reference Manual > Chapter Digital Signature (DS)](#).

---

### Section: External Memory Encryption and Decryption 

#### Subsection 4.1.4.6 - External Memory Encryption and Decryption

The External Memory Encryption and Decryption (XTS_AES) module in the ESP32-C3 chip provides security for users’ application code and data stored in the external memory (flash).

- **Feature List**
  - General XTS_AES algorithm, compliant with IEEE Std 1619-2007
  - Software-based manual encryption
  - High-speed auto decryption, without software’s participation
  - Encryption and decryption functions jointly determined by registers configuration, eFuse parameters, and boot mode

For more details, see the [ESP32-C3 Technical Reference Manual > Chapter External Memory Encryption and Decryption (XTS_AES)](#).

---

**Footer:**
- Espressif Systems
- Page number: 44
- Document title: ESP32-C3 Series Datasheet v2.2

[Submit Documentation Feedback](#)