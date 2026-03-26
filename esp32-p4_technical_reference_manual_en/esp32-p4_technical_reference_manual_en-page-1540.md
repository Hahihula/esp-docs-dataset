

```markdown
| offset | Register                     | offset | Register                     |
|--------|------------------------------|--------|-------------------------------|
| 0x00   | XTS_AES_PLAIN_O_REG          | 0x20   | XTS_AES_PLAIN_8_REG           |
| 0x04   | XTS_AES_PLAIN_1_REG          | 0x24   | XTS_AES_PLAIN_9_REG           |
| 0x08   | XTS_AES_PLAIN_2_REG          | 0x28   | XTS_AES_PLAIN_10_REG          |
| 0x0C   | XTS_AES_PLAIN_3_REG          | 0x2C   | XTS_AES_PLAIN_11_REG          |
| 0x10   | XTS_AES_PLAIN_4_REG          | 0x30   | XTS_AES_PLAIN_12_REG          |
| 0x14   | XTS_AES_PLAIN_5_REG          | 0x34   | XTS_AES_PLAIN_13_REG          |
| 0x18   | XTS_AES_PLAIN_6_REG          | 0x38   | XTS_AES_PLAIN_14_REG          |
| 0x1C   | XTS_AES_PLAIN_7_REG          | 0x3C   | XTS_AES_PLAIN_15_REG          |

## 32.4.5 Manual Encryption Block

The Manual Encryption block is a peripheral module. It is equipped with registers and can be accessed by the CPU directly. Registers embedded in this block, the System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this module. Please note that the Manual Encryption block can only encrypt for storage in the external flash.

The Manual Encryption block is operational only under certain conditions:

*   In SPI Boot mode:
    If bit `HP_SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT` in register `HP_SYSTEM_CRYPTO_CTRL_REG` is 1, the Manual Encryption block can be enabled. Otherwise, it is not operational.
*   In Joint Download Boot mode:
    If bit `HP_SYSTEM_ENABLE_DOWNLOAD_MANUAL_ENCRYPT` in register `HP_SYSTEM_CRYPTO_CTRL_REG` is 1 and the eFuse parameter `EFUSE_DIS_DOWNLOAD_MANUAL_ENCRYPT` is 0, the Manual Encryption block can be enabled. Otherwise, it is not operational.

**Note:**
Even though the CPU can skip cache and get the encrypted instruction/data directly by reading the external memory, users can by no means access Key.

## 32.4.6 Auto Encryption Block

The Auto Encryption block is not a conventional peripheral, so it does not have any registers and cannot be accessed by the CPU directly. The System Registers peripheral, eFuse parameters, and boot mode jointly configure and use this block.

The Auto Encryption block is operational only under certain conditions:

*   In SPI Boot mode:
    when `EFUSE_SPI_BOOT_CRYPTO_CNT` (3 bits) is set to 1, 2, 4 or 7 (i.e., there is an odd number of 1s in its binary representation), then the Auto Encryption block can be enabled. Otherwise, it is not operational.
```