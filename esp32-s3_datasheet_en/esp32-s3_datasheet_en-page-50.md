**Title: Functional Description**

---

### **4.1.4.6 Digital Signature**

A Digital Signature is used to verify the authenticity and integrity of a message using a cryptographic algorithm.

- Feature List:
  - RSA Digital Signatures with key length up to 4096 bits
  - Encrypted private key data, only decryptable by DS peripheral
  - SHA-256 digest to protect private key data against tampering by an attacker

For details, see [ESP32-S3 Technical Reference Manual > Chapter Digital Signature](#).

---

### **4.1.4.7 External Memory Encryption and Decryption**

ESP32-S3 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard.

- Feature List:
  - General XTS-AES algorithm, compliant with IEEE Std 1619-2007
  - Software-based manual encryption
  - High-speed auto encryption, without software’s participation
  - High-speed auto decryption, without software's participation
  - Encryption and decryption functions jointly determined by registers configuration, eFuse parameters, and boot mode

For details, see [ESP32-S3 Technical Reference Manual > Chapter External Memory Encryption and Decryption](#).

---

### **4.1.4.8 Clock Glitch Detection**

The Clock Glitch Detection module on ESP32-S3 monitors input clock signals from XTAL_CLK. If it detects a glitch with a width shorter than 3 ns, input clock signals from XTAL_CLK are blocked.

For details, see [ESP32-S3 Technical Reference Manual > Chapter Clock Glitch Detection](#).

---

### **4.1.4.9 Random Number Generator**

The random number generator (RNG) in ESP32-S3 generates true random numbers, which means random number generated from a physical process, rather than by means of an algorithm. No number generated within the specified range is more or less likely to appear than any other number.

For details, see [ESP32-S3 Technical Reference Manual > Chapter Random Number Generator](#).

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number:** 50  
**Document Title:** ESP32-S3 Series Datasheet v2.1