

```markdown
Register 19.4. AES_MODE_REG (0x0040)

| Bit | Description       |
|-----|-------------------|
| 3   | AES_MODE          |

AES_MODE Configures the key length and encryption/decryption of the AES accelerator.
- 0: AES-128 encryption
- 1: Reserved
- 2: AES-256 encryption
- 3: Reserved
- 4: AES-128 decryption
- 5: Reserved
- 6: AES-256 decryption
- 7: Reserved

(R/W)

Register 19.5. AES_DMA_ENABLE_REG (0x0090)

| Bit | Description             |
|-----|-------------------------|
| 1   | AES_DMA_ENABLE          |

AES_DMA_ENABLE Configures the working mode of the AES accelerator.
- 0: Typical AES
- 1: DMA-AES

(R/W)
```