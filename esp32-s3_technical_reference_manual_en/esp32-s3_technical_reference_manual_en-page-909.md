**Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Diagram Title:**
Figure 23.3-1. External Memory Encryption and Decryption Operation Settings

**Diagram Labels:**
- SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT
- SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT
- Manual Encryption
- Auto Encryption
- eFuse Controller
- System Register (connected to SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT)
- Boot Mode
- Auto Decryption (connected to SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT, EFUSE_SPI_BOOT_CRYPT_CNT)

**Body Text:**
The Manual Encryption block can encrypt instructions/data which will then be written to the external flash as ciphertext via SPI1.

When the CPU writes data to the external RAM through cache, the Auto Encryption block will automatically encrypt the data first, then the data will be written to the external RAM as ciphertext. When the CPU reads from the external flash or external RAM through cache, the Auto Decryption block will automatically decrypt the ciphertext to retrieve instructions and data.

In the System Registers (SYSREG) peripheral, the following four bits in register SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG are relevant to the external memory encryption and decryption:
- SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT
- SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT
- SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT
- SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT

The XTS_AES module also fetches two parameters from the peripheral eFuse Controller, which are: EFUSE_DIS DOWNLOAD_MANUAL_ENCRYPT and EFUSE_SPI_BOOT_CRYPT_CNT.

**Subtitles:**
23.4 Functional Description  
23.4.1 XTS Algorithm

**Additional Text under Subtitle 23.4.1:**
The manual encryption and auto encryption/decryption all use the same algorithm, i.e., XTS algorithm. During implementation, the XTS algorithm is characterized by a "data unit" of 1024 bits, which is defined in the

**Footer Information:**
Espressif Systems  
909  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)