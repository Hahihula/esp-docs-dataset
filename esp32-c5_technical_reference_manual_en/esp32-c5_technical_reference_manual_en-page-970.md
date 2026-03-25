

```markdown
## 29.4.5 Manual Encryption Block

The Manual Encryption block is a peripheral module. It is equipped with registers and can be accessed by the CPU directly. Registers embedded in this block, the System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this module.

The Manual Encryption block is operational only under certain conditions:

*   In SPI Boot mode:
    If bit `HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT` in register
    `HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1, the Manual Encryption block can be enabled. Otherwise, it is not operational.
*   In Download Boot mode:
    If bit `HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT` in register
    `HP_SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1 and the eFuse parameter
    `EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT` is 0, the Manual Encryption block can be enabled. Otherwise, it is not operational.

**Note:**
Even though the CPU can skip cache and get the encrypted instruction/data directly by reading the external memory, users can by no means access Key.

## 29.4.6 Auto Encryption Block

The Auto Encryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this block.

The Auto Encryption block is operational only under certain conditions:

*   In SPI Boot mode:
    when `EFUSE_SPI_BOOT_QRY_CNT` (3 bits in total) is set to 1, 2,4 or 7 (i.e., there is an odd number of 1s in its binary representation), then the Auto Encryption block can be enabled. Otherwise, it is not operational.
*   In Joint Download Boot mode:
    If bit `SYSTEM_ENABLE_DOWNLOAD_DB_ENCRYPT` in register
    `SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG` is 1, the Auto Encryption block can be enabled. Otherwise, it is not operational.

**Note:**
*   When the Auto Encryption block is enabled, it automatically encrypts data written by the CPU to external RAM. The encrypted data is stored in the external RAM, and this encryption process is fully hardware-based, requiring no software intervention. The operation is transparent to the cache, and the encryption key remains inaccessible to the user during the process.
*   When the Auto Encryption block is disabled, it bypasses the CPU’s access request to the cache and does not
```