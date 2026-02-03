**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Note Section in Chapter Header:**
EFUSE_DIS DOWNLOAD MANUAL ENCRYPT is O, the Manual Encryption block can be enabled. Otherwise, it is not operational.

**Section Heading with Note:**
23.4.6 Auto Encryption Block

**Body Text of Section 23.4.6:**
The Auto Encryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers (SYSREG) peripheral, eFuse parameters, and boot mode jointly configure and use this block.

- **Subheading:** In SPI Boot mode
  - If the first bit or the third bit in parameter SPI_BOOT_CRYPTO_CNT (3 bits) is set to 1, then the Auto Encryption block can be enabled. Otherwise, it is not operational.
  
- **Subheading:** In Download Boot mode
  - If bit SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT in register SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG is 1, the Auto Encryption block can be enabled. Otherwise, it is not operational.

**Note Section at Bottom of 23.4.6:**
- When the Auto Encryption block is enabled, it will automatically encrypt data if the CPU writes data to the external RAM, and then the encrypted ciphertext will be written to the external RAM. The entire encryption process does not need software participation and is transparent to the cache. Users can by no means obtain the encryption Key during the process.
- When the Auto Encryption block is disabled, it will ignore the CPU’s access request to cache and do not process the data. Therefore, the data will be written to the external RAM as plaintext directly.

**Section Heading with Note:**
23.4.7 Auto Decryption Block

**Body Text of Section 23.4.7:**
The Auto Decryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers (SYSREG) peripheral, eFuse parameters, and boot mode jointly configure and use this block.

- **Subheading:** In SPI Boot mode
  - If the first bit or the third bit in parameter SPI_BOOT_CRYPTO_CNT (3 bits) is set to 1, then the Auto Decryption block can be enabled. Otherwise, it is not operational.
  
- **Subheading:** In Download Boot mode

**Footer:**
Espressif Systems
913 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback