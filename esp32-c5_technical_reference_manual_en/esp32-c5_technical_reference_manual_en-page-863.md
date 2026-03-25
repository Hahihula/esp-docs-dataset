

```markdown
## 22.4 AES Working Modes

The AES accelerator integrated in ESP32-C5 has two working modes, which are **Typical AES** and **DMA-AES**.

### Typical AES Working Mode:
- Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in NIST FIPS 197.
In this working mode, the plaintext and ciphertext is written and read via CPU directly.

### DMA-AES Working Mode:
- Supports encryption and decryption using cryptographic keys of 128 and 256 bits, specified in NIST FIPS 197;
- Supports block cipher modes ECB, CBC, OFB, CTR, CFB8, and CFB128 under NIST SP 800-38A.
In this working mode, the plaintext and ciphertext are written and read via DMA. An interrupt will be generated when operation completes.

Users can choose the working mode for AES accelerator by configuring the `AES_DMA_ENABLE_REG` register according to Table 22.4-1 below.

**Table 22.4-1. AES Accelerator Working Mode**

| AES_DMA_ENABLE_REG | Working Mode |
|--------------------|--------------|
| 0                  | Typical AES  |
| 1                  | DMA-AES      |

Users can choose the length of cryptographic keys and encryption/decryption by configuring the `AES_MODE_REG` register according to Table 22.4-2 below.

**Table 22.4-2. Key Length and Encryption/Decryption**

| AES_MODE_REG[2:0] | Key Length and Encryption / Decryption |
|-------------------|-----------------------------------------|
| 0                 | AES-128 encryption                      |
| 1                 | reserved                                |
| 2                 | AES-256 encryption                      |
| 3                 | reserved                                |
| 4                 | AES-128 decryption                      |
| 5                 | reserved                                |
| 6                 | AES-256 decryption                      |
| 7                 | reserved                                |

For a detailed introduction to these two working modes, please refer to Section 22.5 and Section 22.6 below.
```