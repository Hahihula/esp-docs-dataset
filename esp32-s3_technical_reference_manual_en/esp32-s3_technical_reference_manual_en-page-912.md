**Title: Chapter 23 External Memory Encryption and Decryption (XTS_AES)**

**Body Text:**
registers block which consists of 16 registers, i.e., XTS_AESPLAIN_n_REG (n=0-15), that are dedicated to data padding and can store up to 512 bits of plaintext instructions/data.

Actually, the Manual Encryption block does not care where the plaintext comes from, but only where the ciphertext will be stored. Because of the strict correspondence between plaintext and ciphertext, in order to better describe how the plaintext is stored in the register block, we assume that the plaintext is stored in the target memory space in the first place and replaced by ciphertext after encryption. Therefore, the following description no longer has the concept of “plaintext”, but uses "target memory space" instead. Please note that the plaintext can come from everywhere in actual use, but users should understand how the plaintext is stored in the register block.

**Subtitle: How mapping works between target memory space and registers**

Assume a word in the target memory space is stored in address, define ofset = address%64, n = offset/4, then the word will be stored in register XTS_AESPLAIN_n_REG.

For example, if the size of the target memory space is 64, then all the 16 registers will be used for data storage. The mapping between ofset and registers is shown in Table 23.4-2.

**Table:**
| ofset | Register           | off set | Register |
|--------|--------------------|---------|----------|
| 0x00   | XTS_AESPLAIN_0_REG | 0x20    | XTS_AESPLAIN_8_REG |
| 0x04   | XTS_AESPLAIN_1_REG | 0x24    | XTS_AESPLAIN_9_REG |
| 0x08   | XTS_AESPLAIN_2_REG | 0x28    | XTS_AESPLAIN_10_REG |
| 0x0C   | XTS_AESPLAIN_3_REG | 0x2C    | XTS_AESPLAIN_11_REG |
| 0x10   | XTS_AESPLAIN_4_REG | 0x30    | XTS_AESPLAIN_12_REG |
| 0x14   | XTS_AESPLAIN_5_REG | 0x34    | XTS_AESPLAIN_13_REG |
| 0x18   | XTS_AESPLAIN_6_REG | 0x38    | XTS_AESPLAIN_14_REG |
| 0x1C   | XTS_AESPLAIN_7_REG | 0x3C    | XTS_AESPLAIN_15_REG |

**Subtitle: Manual Encryption Block**

The Manual Encryption block is a peripheral module. It is equipped with registers and can be accessed by the CPU directly. Registers embedded in this block, the System Registers (SYSREG) peripheral, eFuse parameters, and boot mode jointly configure and use this module. Please note that the Manual Encryption block can only encrypt for storage in the external flash.

The Manual Encryption block is operational only under certain conditions. The operating conditions are:

- In SPI Boot mode
  - If bit SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT in register SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG is 1, the Manual Encryption block can be enabled. Otherwise, it is not operational.
  
- In Download Boot mode
  - If bit SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT in register SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG is 1 and the eFuse parameter

**Footer:**
Espressif Systems  
912  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)