**Title: Functional Description**

---

### **4.1.4.6 Digital Signature Algorithm**

A Digital Signature Algorithm (DSA) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device’s identity to a server, or to check the integrity of a message.

ESP32-C5 includes a DSA module providing hardware acceleration of messages’ signatures based on RSA. HMAC is used as the key derivation function to output the DS_KEY key using eFuse as the input key. Subsequently, the DS module uses DS_KEY to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that neither the decryption key for the RSA parameters nor the input key for the HMAC key derivation function can be seen by users while calculating the signature.

**Feature List**
- RSA digital signatures with key length up to 3072 bits
- encrypted private key data, only decryptable by DS module
- SHA-256 digest to protect private key data against tampering by an attacker

For more details, see the [ESP32-C5 Technical Reference Manual](#) > Chapter Digital Signature Algorithm (DSA).

---

### **4.1.4.7 Elliptic Curve Digital Signature Algorithm**

In cryptography, the Elliptic Curve Digital Signature Algorithm (ECDSA) offers a variant of the Digital Signature Algorithm (DSA) which uses elliptic-curve cryptography.

ESP32-C5’s ECDSA accelerator provides a secure and efficient environment for computing ECDSA signatures. It offers fast computations while ensuring the confidentiality of the signing process to prevent information leakage. This makes it a valuable tool for applications that require high-speed cryptographic operations with strong security guarantees. By using the ECDSA accelerator, users can be confident that their data is being protected without sacrificing performance.

**Feature List**
- digital signature generation and verification
- public key exportation
- three elliptic curves, namely P-192, P-256, and P-384 defined in [FIPS 186-3](#)
- four hash algorithms for message hash in the ECDSA operation, namely SHA-224, SHA-256, SHA-384, and SHA-512 defined in [FIPS PUB 180-4](#)
- deterministic ECDSA defined in [RFC6979](#)

**high security features:**
- dynamic access permission in different operation statuses to ensure information security, preventing key leakage due to intermediate data leakage
- fixed-duration signing and verification processes to resist side-channel attacks

---

Espressif Systems  
47  
[Submit Documentation Feedback](#) ESP32-C5 Series Datasheet v1.0