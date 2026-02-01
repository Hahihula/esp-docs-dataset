**Title: Functional Description**

---

### **4.1.4.5 SHA Accelerator**

The SHA Accelerator (SHA) is a hardware device that significantly speeds up the SHA algorithm compared to software-only implementations.

#### Feature List

- Support for multiple SHA algorithms: SHA-1, SHA-224, and SHA-256
- Two working modes: Typical SHA based on CPU and DMA-SHA based on DMA

For details, see [ESP32-H2 Technical Reference Manual > Chapter SHA Accelerator (SHA)](#).

---

### **4.1.4.6 Digital Signature**

The Digital Signature (DS) module in the ESP32-H2 chip generates message signatures based on RSA with hardware acceleration.

#### Feature List

- RSA digital signatures with key length up to 3072 bits
- Encrypted private key data, only decryptable by DS module
- SHA-256 digest to protect private key data against tampering by an attacker

For details, see [ESP32-H2 Technical Reference Manual > Chapter Digital Signature (DS)](#).

---

### **4.1.4.7 Elliptic Curve Digital Signature Algorithm (ECDSA)**

In cryptography, the Elliptic Curve Digital Signature Algorithm (ECDSA) offers a variant of the Digital Signature Algorithm (DSA) which uses elliptic-curve cryptography. ESP32-H2’s ECDSA Accelerator provides a secure and efficient environment for computing ECDSA signatures. It offers fast computations while ensuring the confidentiality of the signing process to prevent information leakage.

#### Feature List

- Digital signature generation and verification
- Two different elliptic curves, namely P-192 and P-256
- Dynamic access permission in different operation statuses to ensure information security
- High anti-attack performance. Each time a signature is generated and verified, ECDSA consumes:
  - the same amount of time
  - the same amount of power

For details, see [ESP32-H2 Technical Reference Manual > Chapter Elliptic Curve Digital Signature Algorithm (ECDSA)](#).

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
Page number: ESP32-H2 Series Datasheet v1.2 - 37