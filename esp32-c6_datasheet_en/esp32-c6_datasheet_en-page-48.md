**Title: Functional Description**

- Large-number modular multiplication, operands width up to 3072 bits
- Large-number multiplication, operands width up to 1536 bits
- Operands of different widths

For details, see the [ESP32-C6 Technical Reference Manual](#) > Chapter RSA Accelerator.

---

**4.1.4.5 SHA Accelerator**

The SHA Accelerator (SHA) is a hardware device that significantly speeds up the SHA algorithm compared to software-only implementations.

**Feature List**
- Support for multiple SHA algorithms: SHA-1, SHA-224, and SHA-256
- Two working modes: Typical SHA based on CPU and DMA-SHA based on DMA

For more details, see the [ESP32-C6 Technical Reference Manual](#) > Chapter SHA Accelerator (SHA).

---

**4.1.4.6 Digital Signature**

The Digital Signature (DS) module in the ESP32-C6 chip generates message signatures based on RSA with hardware acceleration.

**Feature List**
- RSA digital signatures with key length up to 3072 bits
- Encrypted private key data, only decryptable by DS module
- SHA-256 digest to protect private key data against tampering by an attacker

For more details, see the [ESP32-C6 Technical Reference Manual](#) > Chapter Digital Signature (DS).

---

**4.1.4.7 External Memory Encryption and Decryption**

The External Memory Encryption and Decryption (XTS_AES) module in the ESP32-C6 chip provides security for users’ application code and data stored in the external memory (flash).

**Feature List**
- General XTS-AES algorithm, compliant with IEEE Std 1619-2007
- Software-based manual encryption
- High-speed auto decryption without software’s participation
- Encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode

Configurable Anti-DPA (Differential Power Analysis)

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C6 Series Datasheet v1.4