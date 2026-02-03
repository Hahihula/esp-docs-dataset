**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Section Titles and Descriptions with Details from Images:**

- **Register 19.4. AES_MODE_REG (0x0040)**
  - **Field Description:** 
    - `AES_MODE`: Defines the key length and encryption/decryption of the AES Accelerator.
      - For details, see Table 19.3-2. (R/W)
  
- **Register 19.5. AES_DMA_ENABLE_REG (0x0090)**
  - **Field Description:** 
    - `AES_DMA_ENABLE`: Defines the working mode of the AES Accelerator.
      - Typically, AES: 1; DMA-AES
      - For details, see Table 19.3-1. (R/W)

- **Register 19.6. AES_BLOCK_MODE_REG (0x0094)**
  - **Field Description:** 
    - `AES_BLOCK_MODE`: Defines the block cipher mode of the AES Accelerator operating under the DMA-AES working mode.
      - For details, see Table 19.5-1. (R/W)

- **Register 19.7. AES_BLOCK_NUM_REG (0x0098)**
  - **Field Description:** 
    - `AES_BLOCK_NUM`: Stores the Block Number of plaintext or ciphertext when the AES Accelerator operates under the DMA-AES working mode.
      - For details, see Section 19.5.4. (R/W)

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Document Version Information:** 
- ESP32-S3 TRM (Version 1.7)