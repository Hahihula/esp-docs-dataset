**Title: Functional Description**

- Large-number modular multiplication, up to 4096 bits
- Large-number multiplication, with operands up to 2048 bits
- Operands of different lengths
- Interrupt on completion of computation

**Subtitle: 4.1.5.5 SHA Accelerator (SHA)**

ESP32-P4 integrates an SHA accelerator, which is a hardware device that speeds up the SHA algorithm significantly, compared with an SHA algorithm implemented solely in software. The SHA accelerator integrated in ESP32-P4 has two working modes, Typical SHA and DMA-SHA.

**Feature List**

- **The following hash algorithms introduced in FIPS PUB 180-4 Spec:**
  - SHA-1
  - SHA-224
  - SHA-256
  - SHA-384
  - SHA-512

- Two working modes:
  - Typical SHA
  - DMA-SHA

- Interleaved function when working in Typical SHA working mode.
- Interrupt function when working in DMA-SHA working mode.

**Subtitle: 4.1.5.6 Digital Signature Algorithm (DSA)**

The Digital Signature Algorithm (DSA) is used to verify the authenticity and integrity of a message using a cryptographic algorithm. This can be used to validate a device's identity to a server or to check the integrity of a message.

ESP32-P4 includes a Digital Signature Algorithm (DSA) module providing hardware acceleration of messages' signatures based on RSA. HMAC is used as the key derivation function (KDF) to output the DSA_KEY key using a key stored in eFuse as the input key. Subsequently, the DSA module uses DSA_KEY to decrypt the pre-encrypted parameters and calculate the signature. The whole process happens in hardware so that all the keys involved during the calculating process cannot be seen by users, guaranteeing the security of the operation.

**Footer:**
Espressif Systems
53 ESP32-P4 Series Datasheet v0.6

[Submit Documentation Feedback]