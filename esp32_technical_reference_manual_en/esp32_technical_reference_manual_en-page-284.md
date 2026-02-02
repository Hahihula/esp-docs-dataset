**Chapter Title:**
Chapter 14 AES Accelerator (AES)

**Section Titles and Content:**

### 14.3.4 Encryption and Decryption Operations

#### Single Operation:
1. Initialize AES_MODE_REG, AES_KEY_n_REG, AES_TEXT_m_REG and AES_ENDIAN_REG.
2. Write 1 to AES_START_REG.
3. Wait until AES_IDLE_REG reads 1.
4. Read results from AES_TEXT_m_REG.

#### Consecutive Operations
Every time an operation is completed, only AES_TEXT_m_REG is modified by the AES Accelerator. Initialization can, therefore, be simplified in a series of consecutive operations:
1. Update contents of AES_MODE_REG, AES_KEY_n_REG and AES_ENDIAN_REG if required.
2. Load AES_TEXT_m_REG.
3. Write 1 to AES_START_REG.
4. Wait until AES_IDLE_REG reads 1.
5. Read results from AES_TEXT_m_REG.

### 14.3.5 Speed
The AES Accelerator requires 11 to 15 clock cycles to encrypt a message block, and 21 or 22 clock cycles to decrypt a message block.

### 14.4 Register Summary

| Name                          | Description                                                                                   | Address       | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|---------------|--------|
| **Configuration registers**   |                                                                                               |               |        |
| AES_MODE_REG                  | Mode of operation of the AES Accelerator                                                      | 0x3FF01008    | R/W    |
| AES_ENDIAN_REG                | Endianness configuration register                                                             | 0x3FF01040    | R/W    |
| **Key registers**            |                                                                                               |               |        |
| AES_KEY_0_REG                 | AES key material register 0                                                                  | 0x3FF01010    | R/W    |
| AES_KEY_1_REG                 | AES key material register 1                                                                  | 0x3FF01014    | R/W    |
| ...                           | ...                                                                                           |               |        |
| **Encrypted/decrypted data registers** |                                                                                               |               |        |
| AES_TEXT_0_REG                | AES encrypted/decrypted data register 0                                                      | 0x3FF01030    | R/W    |
| AES_TEXT_1_REG                | AES encrypted/decrypted data register 1                                                      | 0x3FF01034    | R/W    |
| ...                           | ...                                                                                           |               |        |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback