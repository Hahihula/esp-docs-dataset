**Title: Functional Description**

---

### Feature List

- RSA digital signatures with key length up to 4096 bits
- Encrypted private key data, only decryptable by the DSA module
- SHA-256 digest to protect private key data against tampering by an attacker

---

#### Section Title:
**4.1.5.7 Elliptic Curve Digital Signature Algorithm (ECDSA)**

In cryptography, the Elliptic Curve Digital Signature Algorithm (ECDSA) offers a variant of the Digital Signature Algorithm (DSA) which uses elliptic-curve cryptography.

ESP32-P4's ECDSA accelerator provides a secure and efficient environment for computing ECDSA signatures. It enables high-speed cryptographic operations while preserving the confidentiality of the signing process, effectively minimizing the risk of information leakage. This makes it particularly valuable for applications that demand both strong security and fast performance. With the ECDSA accelerator, users can trust that their data is well protected—without compromising on speed.

---

### Feature List

- Digital signature verification
- Two different elliptic curves, namely P-192 and P-256, defined in [FIPS 186-3 Spec](#)
- Two hash algorithms for message hash in the ECDSA operation; namely SHA-224 and SHA-256, defined in FIPS PUB 180-4 Spec
- Dynamic access permission in different operation statuses to ensure information security

---

#### Section Title:
**4.1.5.8 External Memory Encryption and Decryption (XTS_AES)**

The ESP32-P4 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard algorithm specified in [IEEE Std 1619-2007](#), providing security for users' application code and data stored in the external memory (flash and RAM). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) in the external flash, or store general data in the external RAM.

---

### Feature List

- General XTS-AES algorithm; compliant with [IEEE Std 1619-2007](#)
- Software-based manual encryption
- High-speed auto encryption and decryption without software's participation
- Encryption and decryption functions jointly enabled/disabled by register configuration, eFuse parameters, and boot mode
- Configurable Anti-DPA

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6