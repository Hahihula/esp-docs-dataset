**Chapter Title:**
Chapter 14

**Subheading and Section Titles:**
AES Accelerator (AES)

**Section 14.1 - Introduction**

The AES Accelerator speeds up AES operations significantly, compared to AES algorithms implemented solely in software. The AES Accelerator supports six algorithms of FIPS PUB 197, specifically AES-128, AES-192 and AES-256 encryption and decryption.

**Section 14.2 - Features**

- Supports AES-128 encryption and decryption
- Supports AES-192 encryption and decryption
- Supports AES-256 encryption and decryption
- Supports four variations of key endianness and four variations of text endianness

**Section 14.3 - Functional Description**

**Subsection Title:**
AES Algorithm Operations

**Table (Title): Table 14.3-1. Operation Mode**

| AES_MODE_REG[2:0] | Operation |
|-------------------|-----------|
| 0                 | AES-128 Encryption |
| 1                 | AES-192 Encryption |
| 2                 | AES-256 Encryption |
| 4                 | AES-128 Decryption |
| 5                 | AES-192 Decryption |
| 6                 | AES-256 Decryption |

**Subsection Title:**
Key, Plaintext and Ciphertext

The encryption or decryption key is stored in AES_KEY_n_REG, which is a set of eight 32-bit registers. For AES-128 encryption/decryption, the 128-bit key is stored in AES_KEY_0_REG ~ AES_KEY_3_REG. For AES-192

**Footer:**
Espressif Systems
Submit Documentation Feedback
ESP32 TRM (Version 5.6)