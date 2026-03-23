

```markdown
## Register 18.4. AES_MODE_REG (0x0040)

AES_MODE Defines the key length and encryption / decryption of the AES Accelerator. For details, see Table 18.3-2. (R/W)
```

```markdown
## Register 18.5. AES_DMA_ENABLE_REG (0x0090)

AES_DMA_ENABLE Defines the working mode of the AES Accelerator. 0: Typical AES, 1: DMA-AES. For details, see Table 18.3-1. (R/W)
```

```markdown
## Register 18.6. AES_BLOCK_MODE_REG (0x0094)

AES_BLOCK_MODE Defines the block cipher mode of the AES Accelerator operating under the DMA-AES working mode. For details, see Table 18.5-1. (R/W)
```

```markdown
## Register 18.7. AES_BLOCK_NUM_REG (0x0098)

AES_BLOCK_NUM Stores the Block Number of plaintext or ciphertext when the AES Accelerator operates under the DMA-AES working mode. For details, see Section 18.5.4. (R/W)
```