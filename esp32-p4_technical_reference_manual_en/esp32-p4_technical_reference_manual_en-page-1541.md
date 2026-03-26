

```markdown
- In Joint Download Boot mode:

  when bit `HP_SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT` in register `HP_SYSTEM_CRYPTO_CTRL_REG` is 1, the Auto Encryption block can be enabled. Otherwise, it is not operational.

Note:
* When the Auto Encryption block is enabled, it will automatically encrypt data if the CPU writes data to the external RAM, and then the encrypted ciphertext will be written to the external RAM. The entire encryption process does not need software participation and is transparent to the cache. Users can by no means obtain the encryption `Key` during the process.
* When the Auto Encryption block is disabled, it will ignore the CPU's access request to the cache and not process the data. Therefore, the data will be written to the external RAM as plaintext directly.

## 32.4.7 Auto Decryption Block

The Auto Decryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this block.

The Auto Decryption block is operational only under certain conditions:

* In SPI Boot mode:
  when `EFUSE_SPI_BOOT_CRYPTO_CNT` (3 bits in total) is set to 1, 2,4 or 7 (i.e., there is an odd number of 1s in its binary representation), then the Auto Decryption block can be enabled. Otherwise, it is not operational.
* In Joint Download Boot mode:
  when bit `HP_SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT` in register `HP_SYSTEM_CRYPTO_CTRL_REG` is 1, the Auto Decryption block can be enabled. Otherwise, it is not operational.

Note:
* When the Auto Decryption block is enabled, it will automatically decrypt the ciphertext if the CPU reads instructions/data from the external memory via cache to retrieve the instructions/data. The entire decryption process does not need software participation and is transparent to the cache. The software can by no means obtain the decryption `Key` during the process.
* When the Auto Decryption block is disabled, it does not have any effect on the contents stored in the external memory, no matter if they are encrypted or not. Therefore, what the CPU reads via cache is the original information stored in the external memory.

## 32.5 Software Process

When the Manual Encryption block operates, software needs to be involved in the process. The steps are as follows:
```