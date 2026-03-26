

```markdown
## Register 25.6. AES_BLOCK_MODE_REG (0x0094)

AES_BLOCK_MODE Configures the block cipher mode of the AES accelerator operating under the DMA-AES working mode.

- 0: ECB (Electronic Code Block)
- 1: CBC (Cipher Block Chaining)
- 2: OFB (Output FeedBack)
- 3: CTR (Counter)
- 4: CFB8 (8-bit Cipher FeedBack)
- 5: CFB128 (128-bit Cipher FeedBack)
- 6: GCM (Galois/Counter Mode)
- 7: Reserved

(R/W)

## Register 25.7. AES_BLOCK_NUM_REG (0x0098)

AES_BLOCK_NUM Represents the Block Number of plaintext or ciphertext when the AES accelerator operates under the DMA-AES working mode. For details, see Section 25.6.4. (R/W)

## Register 25.8. AES_INC_SEL_REG (0x009C)

AES_INC_SEL Configures the Standard Incrementing Function for CTR block operation.

- 0: INC32
- 1: INC128

(R/W)
```