

# Chapter 19

## AES Accelerator (AES)

### 19.1 Introduction

ESP32-C6 integrates an Advanced Encryption Standard (AES) accelerator, which is a hardware device that speeds up computation using AES algorithm significantly, compared to AES algorithms implemented solely in software. The AES accelerator integrated in ESP32-C6 has two working modes, which are **Typical AES** and **DMA-AES**.

### 19.2 Features

The following functionality is supported:

*   Typical AES working mode
    -   AES-128/AES-256 encryption and decryption
*   DMA-AES working mode
    -   AES-128/AES-256 encryption and decryption
    -   Block cipher mode
        *   ECB (Electronic Codebook)
        *   CBC (Cipher Block Chaining)
        *   OFB (Output Feedback)
        *   CTR (Counter)
        *   CFB8 (8-bit Cipher Feedback)
        *   CFB128 (128-bit Cipher Feedback)
    -   Interrupt on completion of computation

### 19.3 AES Working Modes

The AES accelerator integrated in ESP32-C6 has two working modes, which are **Typical AES** and **DMA-AES**.

*   Typical AES Working Mode:
    -   Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in [NIST FIPS 197](#).