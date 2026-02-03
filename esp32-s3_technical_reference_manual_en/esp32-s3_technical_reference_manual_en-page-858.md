**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Section Titles and Content:**

- **19.1 Introduction**
  - ESP32-S3 integrates an Advanced Encryption Standard (AES) Accelerator, which is a hardware device that speeds up AES Algorithm significantly, compared to AES algorithms implemented solely in software.
  - The AES Accelerator integrated in ESP32-S3 has two working modes, which are **Typical AES** and **DMA-AES**.

- **19.2 Features**
  - The following functionality is supported:
    - Typical AES working mode
      - AES-128/AES-256 encryption and decryption
    - DMA-AES working mode
      - AES-128/AES-256 encryption and decryption

  **Block cipher mode:**
  - ECB (Electronic Codebook)
  - CBC (Cipher Block Chaining)
  - OFB (Output Feedback)
  - CTR (Counter)
  - CFB8 (8-bit Cipher Feedback)
  - CFB128 (128-bit Cipher Feedback)

- **Interrupt on completion of computation**

- **19.3 AES Working Modes**
  - The AES Accelerator integrated in ESP32-S3 has two working modes, which are Typical AES and DMA-AES.
    - **Typical AES Working Mode:**
      - Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in FIPS 197.

**Additional Information at the Bottom:**
- In this working mode, the plaintext and ciphertext is written and read via CPU directly.
- Espressif Systems
- Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)