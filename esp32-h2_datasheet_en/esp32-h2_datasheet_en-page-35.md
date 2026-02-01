**Title: Functional Description**

- **4.1.4 Cryptography and Security Components**
  This subsection describes the security features incorporated into the chip, which safeguard data and operations.

- **4.1.4.1 AES Accelerator**
  ESP32-H2 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-H2 has two working modes, which are Typical AES and DMA-AES.

- **Feature List**
  - Typical AES working mode
    - AES-128/AES-256 encryption and decryption

  - DMA-AES working mode
    - AES-128/AES-256 encryption and decryption
    - Block cipher mode
      * ECB (Electronic Codebook)
      * CBC (Cipher Block Chaining)
      * OFB (Output Feedback)
      * CTR (Counter)
      * CFB8 (8-bit Cipher Feedback)
      * CFB128 (128-bit Cipher Feedback)

  - Interrupt on completion of computation

- **Anti-attack pseudo-round function, to enhance the chip's anti-attack performance**

For details, see [ESP32-H2 Technical Reference Manual](#) > Chapter AES Accelerator (AES).

- **4.1.4.2 ECC Accelerator**
  The ECC Accelerator accelerates calculations based on the Elliptic Curve Cryptography (ECC) algorithm and ECC-derived algorithms like ECDSA, which offers the advantages of smaller public keys compared to RSA cryptography with equivalent security.

**Footer:**
Espressif Systems
35 ESP32-H2 Series Datasheet v1.2

[Submit Documentation Feedback](#)