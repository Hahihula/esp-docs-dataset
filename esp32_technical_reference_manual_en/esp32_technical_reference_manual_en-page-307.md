**Chapter Title:**
Chapter 17 External Memory Encryption and Decryption (FLASH)

**Section Header:**
For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Register Information Table:**

- **Register Name:** FLASH_ENCRYPTION_BUFFER_n_REG  
  **Description:** Data buffers for encryption. (WO)  
  **Address:** n: 0-7 (0x0+4*n)  
  **Example Value:** 31, 0x00000000

- **Register Name:** FLASH_ENCRYPTION_START_REG  
  **Description:** FLASH_ENCRYPTION_START_REG (0x020)  
  **Bit Description:** FLASH_START Set this bit to start encryption operation on data buffer. (WO)  
  **Example Value:** 31, 0x00000000

- **Register Name:** FLASH_ENCRYPTION_ADDRESS_REG  
  **Description:** The physical address on the off-chip flash must be 8-word boundary aligned. (WO)  
  **Address:** 0x024  
  **Example Value:** 31, 0x00000000

- **Register Name:** FLASH_ENCRYPTION_DONE_REG  
  **Description:** FLASH_ENCRYPTIONDone Reg (0x028)  
  **Bit Description:** FLASH_DONE Set this bit when encryption operation is complete. (RO)  
  **Example Value:** 31, 0x00000000

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback