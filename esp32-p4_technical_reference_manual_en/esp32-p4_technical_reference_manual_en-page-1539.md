

```markdown
## 32.4.3 Target Memory Space

The target memory space refers to a continuous address space in the external memory where the first encrypted ciphertext is stored. The target memory space can be uniquely determined by three relevant parameters: type, size, and base address, whose definitions are listed below.

- Type: the `type` of the target memory space, either external flash or external RAM. Value 0 indicates external flash, while 1 indicates external RAM.
- Size: the `size` of the target memory space, indicating the number of bytes encrypted in one encryption operation, which supports 16, 32, or 64 bytes.
- Base address: the `base_addr` of the target memory space. It is a 30-bit physical address, with a range of `0x0000_0000 ~ 0x3FFF_FFFF`. It should be aligned to `size`, i.e., `base_addr % size == 0`.

For example, if there are 16 bytes of instruction data that need to be encrypted and written to address `0x130 ~ 0x13F` in the external flash, then the target space is `0x130 ~ 0x13F`, type is 0 (external flash), size is 16 (bytes), and the base address is `0x130`.

The encryption of any length (must be multiples of 16 bytes) of plaintext instruction/data can be completed separately in multiple operations, and each operation has individual target memory space and relevant parameters.

For Auto Encryption/Decryption blocks, these parameters are automatically defined by hardware. For the Manual Encryption block, these parameters should be configured manually by users.

**Note:**
The “tweak” defined in Chapter 5.1 Data units and tweaks of IEEE Std 1619-2007 is a 128-bit non-negative integer (`tweak`), which can be generated according to `tweak = type * 2^30 + (base_addr & 0x3FFFFF80)`. The lowest 7 bits and the highest 97 bits in `tweak` are always zero.

## 32.4.4 Data Writing

For Auto Encryption/Decryption blocks, data writing is automatically applied in hardware. For Manual Encryption blocks, data writing should be applied by users. The Manual Encryption block has a register block which consists of 16 registers, i.e., `XTS_AES_PLAIN_n_REG` (`n: 0 ~ 15`), that are dedicated to data writing and can store up to 512 bits of plaintext at a time.

Actually, the Manual Encryption block does not care where the plaintext comes from, but only where the ciphertext will be stored. Because of the strict correspondence between plaintext and ciphertext, in order to better describe how the plaintext is stored in the register block, we assume that the plaintext is stored in the target memory space in the first place and replaced by ciphertext after encryption. Therefore, the following description in this section no longer has the concept of “plaintext”, but uses “target memory space” instead.

**How mapping between target memory space and registers works:**

Assume a word in the target memory space is stored in `address`, define `offset = address % 64`, `n = offset / 4`, then the word will be stored in register `XTS_AES_PLAIN_n_REG`.

For example, when the `size` is 64, all registers in the register block will be used. The mapping between `offset` and registers now is shown in Table 32.4-2.
```