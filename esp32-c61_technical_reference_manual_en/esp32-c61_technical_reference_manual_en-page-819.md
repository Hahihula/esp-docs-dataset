

```markdown
process the data. As a result, data is written directly to external RAM in plaintext.
```

## 23.4.7 Auto Decryption Block

The Auto Decryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this block.

The Auto Decryption block is operational only under certain conditions:

* In SPI Boot mode
  when `EFUSE_SPI_BOOT_CRYPTO_CNT` (3 bits in total) is set to 1, 2,4 or 7 (i.e., there is an odd number of 1s in its binary representation), then the Auto Decryption block can be enabled. Otherwise, it is not operational.
* In Download Boot mode
  when bit `HP_SYS_ENABLE_DOWNLOAD_GOCB_DECRYPT` in register `HP_SYS_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1, the Auto Decryption block can be enabled. Otherwise, it is not operational.

**Note:**
* When the Auto Decryption block is enabled, it automatically decrypts encrypted data or instructions read by the CPU from external memory via the cache. This decryption process is hardware-based and requires no software intervention, remaining transparent to the cache. The decryption key is not accessible to the software during this process.
* When the Auto Decryption block is disabled, it does not affect the contents stored in external memory, regardless of whether they are encrypted. Consequently, the CPU reads the original data stored in external memory via the cache.

## 23.5 Software Process

When the Manual Encryption block operates, software needs to be involved in the process. The steps are as follows:

1. Configure XTS_AES:
    * Write 0 to register `XTS_AES_DESTINATION_REG`.
    * Set register `XTS_AES_PHYSICAL_ADDRESS_REG` to `base_addr`.
    * Set register `XTS_AES_LINESIZE_REG` to `$size/32$`.

      For definitions of `base_addr` and `size`, please refer to Section 23.4.3.

2. Write plaintext instructions/data to the registers block `XTS_AES_PLAIN_n_REG` (n: 0-15). For detailed information, please refer to Section 23.4.4.
    Please write data to registers according to your actual needs, and the unused ones could be set to arbitrary values.
```