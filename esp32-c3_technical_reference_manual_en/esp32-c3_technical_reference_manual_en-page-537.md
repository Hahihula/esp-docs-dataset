

```markdown
(tweak), which can be generated according to tweak = (base_addr & 0x00FFFF80). The lowest 7 bits and the highest 97 bits in tweak are always zero.

## 23.4.4 Data Writing

For Auto Decryption blocks, data writing is automatically applied in hardware. For Manual Encryption blocks, data writing should be applied by users. The Manual Encryption block has a register block which consists of 8 registers, i.e., XTS_AES_PLAIN_n_REG (n: 0 ~ 7), that are dedicated to data writing and can store up to 256 bits of plaintext at a time.

Actually, the Manual Encryption block does not care where the plaintext comes from, but only where the ciphertext will be stored. Because of the strict correspondence between plaintext and ciphertext, in order to better describe how the plaintext is stored in the register block, we assume that the plaintext is stored in the target memory space in the first place and replaced by ciphertext after encryption. Therefore, the following description no longer has the concept of “plaintext”, but uses “target memory space” instead. Please note that the plaintext can come from everywhere in actual use, but users should understand how the plaintext is stored in the register block.

**How mapping between target memory space and registers works:**

Assume a word in the target memory space is stored in address, define offset = address % 32, n = offset / 4, then the word will be stored in register XTS_AES_PLAIN_n_REG.

The mapping between offset and registers is shown in Table 23.4-2.

Table 23.4-2. Mapping Between Offsets and Registers

| offset | Register                  | offset | Register                 |
|--------|---------------------------|--------|--------------------------|
| 0x00   | XTS_AES_PLAIN_0_REG       | 0x10   | XTS_AES_PLAIN_4_REG      |
| 0x04   | XTS_AES_PLAIN_1_REG       | 0x14   | XTS_AES_PLAIN_5_REG      |
| 0x08   | XTS_AES_PLAIN_2_REG       | 0x18   | XTS_AES_PLAIN_6_REG      |
| 0x0C   | XTS_AES_PLAIN_3_REG       | 0x1C   | XTS_AES_PLAIN_7_REG      |

## 23.4.5 Manual Encryption Block

The Manual Encryption block is a peripheral module. It is equipped with registers and can be accessed by the CPU directly. Registers embedded in this block, the System Registers (SYSREG) peripheral, eFuse parameters, and boot mode jointly configure and use this module. Please note that the Manual Encryption block can only encrypt for storage in external flash.

The Manual Encryption block is operational only under certain conditions. The operating conditions are:

*   In SPI Boot mode
    If bit SYSTEM_ENABLE_SPI_MANUAL_ENCRYPT in register SYSTEM_EXTERNAL_DEVICE_ENCRYPT_DECRYPT_CONTROL_REG is 1, the Manual Encryption block can be enabled. Otherwise, it is not operational.
*   In Download Boot mode

Espressif Systems
537
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```