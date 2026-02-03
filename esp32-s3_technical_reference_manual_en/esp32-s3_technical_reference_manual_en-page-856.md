**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Header:**
GoBack

**Register Information Section**

- **Register Name:** Register 18.9. SHA_MODE_REG (0x0000)
  - Description: (reserved)  
  - Binary Representation Diagram:
    ```
    3 | 2 | 1
    0 x0
    ```

- **Field Definition for SHA_MODE:**
  - **Name:** SHA_MODE
  - **Description:** Defines the SHA algorithm. For details, please see Table 18.3-2 (R/W)

- **Register Name:** Register 18.10. SHA_T_STRING_REG (0x0004)
  - Description: 
    ```
    3 | 2
    0 x0
    ```

- **Field Definition for SHA_T_STRING:**
  - **Name:** SHA_T_STRING
  - **Description:** Defines t_string for calculating the initial Hash value for SHA-512/t. (R/W)

- **Register Name:** Register 18.11. SHA_T_LENGTH_REG (0x0008)
  - Description: 
    ```
    7 | 6
    0 x0
    ```

- **Field Definition for SHA_T_LENGTH:**
  - **Name:** SHA_T_LENGTH
  - **Description:** Defines t_length for calculating the initial Hash value for SHA-512/t. (R/W)

- **Register Name:** Register 18.12. SHA_DMA_BLOCK_NUM_REG (0x000C)
  - Description: 
    ```
    6 | 5
    0 x0
    ```

- **Field Definition for SHA_DMA_BLOCK_NUM:**
  - **Name:** SHA_DMA_BLOCK_NUM
  - **Description:** Defines the DMA-SHA block number. (R/W)

**Footer Information:**
Espressif Systems  
856 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback