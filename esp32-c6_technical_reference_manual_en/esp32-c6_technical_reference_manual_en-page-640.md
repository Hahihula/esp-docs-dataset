

```markdown
## Table 19.3-1. AES Accelerator Working Mode

| AES_DMA_ENABLE_REG | Working Mode |
|--------------------|--------------|
| 0                  | Typical AES  |
| 1                  | DMA-AES      |

## Table 19.3-2. Key Length and Encryption/Decryption

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

**Notice:**
ESP32-C6's Digital Signature (DS) module will call the AES accelerator. Therefore, users cannot access the AES accelerator when Digital Signature (DS) module is working.
```