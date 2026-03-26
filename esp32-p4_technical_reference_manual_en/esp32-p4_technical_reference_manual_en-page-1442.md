

```markdown
Register 25.4. AES_MODE_REG (0x0040)

| Bit | Field     | Description                  |
|-----|-----------|------------------------------|
| 31  |           | (reserved)                   |
| 3   | AES_MODE  | Configures the key length and encryption/decryption of the AES accelerator.<br>0: AES-128 encryption<br>1: Reserved<br>2: AES-256 encryption<br>3: Reserved<br>4: AES-128 decryption<br>5: Reserved<br>6: AES-256 decryption<br>7: Reserved<br>(R/W) |

Register 25.5. AES_DMA_ENABLE_REG (0x0090)

| Bit | Field               | Description                                      |
|-----|---------------------|--------------------------------------------------|
| 31  |                     | (reserved)                                      |
| 1   | AES_DMA_ENABLE      | Configures the working mode of the AES accelerator.<br>0: Typical AES<br>1: DMA-AES<br>(R/W) |
```