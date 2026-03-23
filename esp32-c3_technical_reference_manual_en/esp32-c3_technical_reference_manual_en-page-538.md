

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack


If bit `SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT` in register  
`SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1 and the eFuse parameter  
`EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT` is 0, the Manual Encryption block can be enabled.  
Otherwise, it is not operational.


Note:

* Even though the CPU can skip cache and get the encrypted instruction/data directly by reading the external memory, users can by no means access `Key`.


23.4.6 Auto Decryption Block

The Auto Decryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers (SYSREG) peripheral, eFuse parameters, and boot mode jointly configure and use this block.

The Auto Decryption block is operational only under certain conditions. The operating conditions are:

* In SPI Boot mode

  If the first bit or the third bit in parameter `SPI_BOOT_CRYPT_CNT` (3 bits) is set to 1, then the Auto Decryption block can be enabled. Otherwise, it is not operational.

* In Download Boot mode

  If bit `SYSTEM_ENABLE_DOWNLOAD_GOCB_DECRYPT` in register  
  `SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1, the Auto Decryption block can be enabled. Otherwise, it is not operational.


Note:

* When the Auto Decryption block is enabled, it will automatically decrypt the ciphertext if the CPU reads instructions/data from the external memory via cache to retrieve the instructions/data. The entire decryption process does not need software participation and is transparent to the cache. Users can by no means obtain the decryption `Key` during the process.
* When the Auto Decryption block is disabled, it does not have any effect on the contents stored in the external memory, no matter if they are encrypted or not. Therefore, what the CPU reads via cache is the original information stored in the external memory.


23.5 Software Process

When the Manual Encryption block operates, software needs to be involved in the process. The steps are as follows:

1. Configure XTS_AES:
    * Set register `XTS_AES_PHYSICAL_ADDRESS_REG` to `base_addr`.
    * Set register `XTS_AES_LINESIZE_REG` to `size/32`.

For definitions of `base_addr` and `size`, please refer to Section 23.4.3.
```