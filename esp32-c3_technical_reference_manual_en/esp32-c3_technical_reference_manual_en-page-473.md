

```markdown
Chapter 18  
AES Accelerator (AES)

## Chapter 18

### AES Accelerator (AES)

#### 18.1 Introduction

ESP32-C3 integrates an Advanced Encryption Standard (AES) Accelerator, which is a hardware device that speeds up AES Algorithm significantly, compared to AES algorithms implemented solely in software. The AES Accelerator integrated in ESP32-C3 has two working modes, which are **Typical AES** and **DMA-AES**.

#### 18.2 Features

The following functionality is supported:

*   Typical AES working mode
    *   AES-128/AES-256 encryption and decryption
*   DMA-AES working mode
    *   AES-128/AES-256 encryption and decryption
*   Block cipher mode
    *   ECB (Electronic Codebook)
    *   CBC (Cipher Block Chaining)
    *   OFB (Output Feedback)
    *   CTR (Counter)
    *   CFB8 (8-bit Cipher Feedback)
    *   CFB128 (128-bit Cipher Feedback)
        *   Interrupt on completion of computation

#### 18.3 AES Working Modes

The AES Accelerator integrated in ESP32-C3 has two working modes, which are **Typical AES** and **DMA-AES**.

*   Typical AES Working Mode:
    *   Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in [NIST FIPS 197](#).

In this working mode, the plaintext and ciphertext is written and read via CPU directly.
```