

```markdown
Chapter 25 External Memory Encryption and Decryption (XTS_AES) GoBack


Figure 25.3-1. Architecture of the External Memory Encryption and Decryption



The Manual Encryption block can encrypt instructions/data which will then be written to the external flash as ciphertext via SPI1.

In the System Registers (HP_SYS) peripheral (see 17 System Registers), the following three bits in register HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG are relevant to the external memory encryption and decryption:

*   `HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT`
*   `HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT`
*   `HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT`

The XTS_AES module also fetches two parameters from the peripheral eFuse Controller, which are: EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT and EFUSE_SPI_BOOT_CRYPT_CNT. For detailed information, please see Chapter 6 eFuse Controller.



25.4 Functional Description

25.4.1 XTS Algorithm

Both manual encryption and auto decryption use the XTS algorithm. During implementation, the XTS algorithm is characterized by a "data unit" of 1024 bits, defined in the Section XTS-AES encryption procedure of XTS-AES Tweakable Block Cipher Standard. For more information about the XTS-AES algorithm, please refer to IEEE Std 1619-2007.
```