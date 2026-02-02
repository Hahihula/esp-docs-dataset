**Chapter Title:**
Chapter 17 External Memory Encryption and Decryption (FLASH)

**Body Text:**

When the Flash Decryption block is operating, the CPU will read instructions and data from the off-chip flash via the cache. The Flash Decryption block automatically decrypts the instructions and data in the cache. The entire decryption process does not need software intervention and is transparent to the cache. The decryption algorithm can decrypt the code that has been encrypted by the Flash Encryption block. Software cannot access the key algorithm `Keyd` used.

When the Flash Decryption block is not operating, it does not have any effect on the contents stored in the off-chip flash; be they encrypted or unencrypted. What the CPU reads via the cache is the original information stored in the off-chip flash.

**Subheading:**
Flash Encryption Operating Conditions:

- During SPI Flash Boot
  - In the efuse system parameter `flash_crypt_cnt` (7 bits wide), if the number of bits with value 1 is odd, the Flash Decryption block is operational. Otherwise, it is not.
  
- During Download Boot
  - If the `DPORT_SPI_DECRYPT_ENABLE` bit in `DPORT_SPI_CONFIG_REG` is 1, and system parameter download_dis_decrypt is 0, the Flash Decryption block is operational. Otherwise, it is not.

**Subheading:**
17.4 Register Summary

The addresses in this section are relative to the External Memory Encryption and Decryption (FLASH) base address provided in Table 3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Title:** 
Register Address Information
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| FLASH_ENCRYPTION_BUFFER_0_REG | Flash encryption buffer register 0 | 0x3FF5B000 | WO |
| FLASH_ENCRYPTION_BUFFER_1_REG | Flash encryption buffer register 1 | 0x3FF5B004 | WO |
| FLASH_ENCRYPTION_BUFFER_2_REG | Flash encryption buffer register 2 | 0x3FF5B008 | WO |
| FLASH_ENCRYPTION_BUFFER_3_REG | Flash encryption buffer register 3 | 0x3FF5B00C | WO |
| FLASH_ENCRYPTION_BUFFER_4_REG | Flash encryption buffer register 4 | 0x3FF5B010 | WO |
| FLASH_ENCRYPTION_BUFFER_5_REG | Flash encryption buffer register 5 | 0x3FF5B014 | WO |
| FLASH_ENCRYPTION_BUFFER_6_REG | Flash encryption buffer register 6 | 0x3FF5B018 | WO |
| FLASH_ENCRYPTION_BUFFER_7_REG | Flash encryption buffer register 7 | 0x3FF5B01C | WO |
| FLASH_ENCRYPTION_START_REG | Encrypt operation control register | 0x3FF5B020 | WO |
| FLASH_ENCRYPTION_ADDRESS_REG | External flash address register | 0x3FF5B024 | WO |
| FLASH_ENCRYPTION_DONE_REG | Encrypt operation status register | 0x3FF5B028 | RO |

**Subheading:**
17.5 Register

The addresses in this section are relative to the External Memory Encryption and Decryption (FLASH) base address provided in Table 3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section 17.4 Register Summary.

**Footer Information:** 
Espressif Systems
Page Number: 306
Document Version: ESP32 TRM (Version 5.6)
Submit Documentation Feedback