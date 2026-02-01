**Title: Functional Description**

---

### Feature List

- Digital signature generation and verification
- Two elliptic curves, namely P-192 and P-256 defined in FIPS 186-3
- Two hash algorithms for message hash in the ECDSA operation, namely SHA-224 and SHA-256 defined in FIPS PUB 180-4

#### High security features:
- Dynamic access permission in different operation statuses to ensure information security, preventing key leakage due to intermediate data leakage.
- Fixed-duration signing and verification processes to resist side-channel attacks.

---

**Subtitle: 4.1.4.3 SHA Accelerator**

ESP32-C61 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared to SHA algorithms implemented solely in software. The SHA accelerator has two working modes, Typical SHA and DMA-SHA.

#### Feature List
- Support for multiple SHA algorithms: SHA-1, SHA-224, and SHA-256.
- Two working modes: Typical SHA based on CPU and DMA-SHA based on DMA.
- Interleaved function in Typical SHA working mode.
- Interrupt function in DMA-SHA working mode.

---

**Subtitle: 4.1.4.4 External Memory Encryption and Decryption**

The ESP32-C61 integrates an External Memory Encryption and Decryption module that complies with the XTS-AES standard algorithm specified in IEEE Std 1619-2007, providing security for users’ application code and data stored in the external memory (flash and PSRAM). Users can store proprietary firmware and sensitive data (e.g., credentials for gaining access to a private network) to the external flash, and securely run data-sensitive applications in PSRAM.

#### Feature List
- General XTS-AES algorithm. compliant with IEEE Std 1619-2007.
- Software-based manual encryption.
- High-speed auto decryption without software.
- Encryption and decryption functions jointly enabled/disabled by registers configuration, eFuse parameters, and boot mode.
- Configurable counter measures against DPA attacks
- Flash and PSRAM use their own separate keys

---

**Footer:**
Espressif Systems  
42 ESP32-C61 Series Datasheet v0.5