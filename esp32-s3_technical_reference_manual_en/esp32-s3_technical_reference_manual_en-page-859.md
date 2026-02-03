**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**GoBack Link:** GoBack

**Subheading and List Item:**
- DMA-AES Working Mode:
  - Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in NIST FIPS 197;
  - Supports block cipher modes ECB/CBC/OFB/CTR/CFB8/CFB128 under NIST SP 800-38A.

**Body Text:**
In this working mode, the plaintext and ciphertext is written and read via DMA. An interrupt will be generated when operation completes.
Users can choose the working mode for AES accelerator by configuring the AES_DMA_ENABLE_REG register according to Table 19.3-1 below.

**Table Title:** Table 19.3-1. AES Accelerator Working Mode

| AES_DMA_ENABLE_REG | Working Mode |
|--------------------|--------------|
| 0                  | Typical AES |
| 1                  | DMA-AES     |

**Body Text:**
Users can choose the length of cryptographic keys and encryption/decryption by configuring the AES_MODE_REG register according to Table 19.3-2 below.

**Table Title:** Table 19.3-2. Key Length and Encryption/Decryption

| AES_MODE_REG | Key Length and Encryption/Decryption |
|--------------|---------------------------------------|
| 0           | AES-128 encryption                     |
| 1           | reserved                               |
| 2           | AES-256 encryption                     |
| 3           | reserved                               |
| 4           | AES-128 decryption                     |
| 5           | reserved                               |
| 6           | AES-256 decryption                     |
| 7           | reserved                               |

**Body Text:**
For detailed introduction on these two working modes, please refer to Section 19.4 and Section 19.5 below.

**Notice Box:** 
Notice: ESP32-S3's Digital Signature (DS) module will call the AES accelerator. Therefore, users cannot access the AES accelerator when Digital Signature (DS) module is working.

**Subheading Title:**
19.4 Typical AES Working Mode

**Body Text:**
In the Typical AES working mode, users can check the working status of the AES accelerator by inquiring the AES_STATE_REG register and comparing the return value against the Table 19.4-1 below.

**Table Title:** Table 19.4-1. Working Status under Typical AES Working Mode

| AES_STATE_REG | Status    | Description |
|---------------|-----------|-------------|
|                |           |             |

**Footer:**
Espressif Systems
859
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)