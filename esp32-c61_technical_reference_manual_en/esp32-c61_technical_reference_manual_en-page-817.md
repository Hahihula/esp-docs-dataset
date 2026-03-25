

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack


For example, if there are 16 bytes of instruction data that need to be encrypted and written to address 0x130 ~ 0x13F in the external flash, then the target space is 0x130 ~ 0x13F, type is 0 (external flash), size is 16 (bytes), and the base address is 0x130.

The encryption of any length (must be multiples of 16 bytes) of plaintext instruction/data can be completed separately in multiple operations, and each operation has its individual target memory space and the relevant parameters.

For Auto Encryption/Decryption blocks, these parameters are automatically determined by hardware. For the Manual Encryption blocks, these parameters should be configured manually by users.


Note:
The “tweak” defined in Chapter 5.1 Data units and tweaks of IEEE Std 1619-2007 is a 128-bit non-negative integer (tweak), which can be generated according to tweak = type * 2^30 + (base_addr & 0x3FFFFFF80). The lowest 7 bits and the highest 97 bits in tweak are always zero.


23.4.4 Data Writing

For Auto Encryption/Decryption blocks, data writing is automatically applied in hardware. For Manual Encryption blocks, data writing should be applied by users. The Manual Encryption block has a register block which consists of 16 registers, i.e., XTS_AES_PLAIN_n_REG (n: 0 ~ 15), that are dedicated to data writing and can store up to 512 bits of plaintext at a time.

Actually, the Manual Encryption block does not care where the plaintext comes from, but only where the ciphertext will be stored. Because of the strict correspondence between plaintext and ciphertext, in order to better describe how the plaintext is stored in the register block, we assume that the plaintext is stored in the target memory space in the first place and replaced by ciphertext after encryption. Therefore, the following description in this section no longer has the concept of “plaintext”, but uses “target memory space” instead.

How mapping between target memory space and registers works:

Assume a word in the target memory space is stored in address, define offset = address%64, n = offset/4, then the word will be stored in register XTS_AES_PLAIN_n_REG.

For example, when the size is 64, all registers in the register block will be used. The mapping between offset and registers now is shown in Table 23.4-2.


Table 23.4-2. Mapping Between Offsets and Registers

| offset | Register                  | offset | Register                  |
|--------|---------------------------|--------|---------------------------|
| 0x00   | XTS_AES_PLAIN_0_REG       | 0x20   | XTS_AES_PLAIN_8_REG       |
| 0x04   | XTS_AES_PLAIN_1_REG       | 0x24   | XTS_AES_PLAIN_9_REG       |
| 0x08   | XTS_AES_PLAIN_2_REG       | 0x28   | XTS_AES_PLAIN_10_REG      |
| 0x0C   | XTS_AES_PLAIN_3_REG       | 0x2C   | XTS_AES_PLAIN_11_REG      |
| 0x10   | XTS_AES_PLAIN_4_REG       | 0x30   | XTS_AES_PLAIN_12_REG      |
| 0x14   | XTS_AES_PLAIN_5_REG       | 0x34   | XTS_AES_PLAIN_13_REG      |
| 0x18   | XTS_AES_PLAIN_6_REG       | 0x38   | XTS_AES_PLAIN_14_REG      |
| 0x1C   | XTS_AES_PLAIN_7_REG       | 0x3C   | XTS_AES_PLAIN_15_REG      |

Espressif Systems
```