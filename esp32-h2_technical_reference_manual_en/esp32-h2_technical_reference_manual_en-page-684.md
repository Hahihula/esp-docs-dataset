

```markdown
## 26.4.2 Key

The Manual Encryption block and Auto Decryption block share the same `Key` when implementing the XTS algorithm. The `Key` is provided by the eFuse hardware and cannot be accessed by software.

The `Key` is 256-bit long. The value of the `Key` is determined by the content in one eFuse block from BLOCK4 ~ BLOCK9. For easier description, we define:

*   `BlockA`: the block whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_128_KEY (please refer to Table 5.3-2 Secure Key Purpose Values). If `BlockA` exists, a 256-bit `KeyA` is stored in it.

There are two possibilities of how the `Key` is generated depending on whether `BlockA` exists or not, as shown in Table 26.4-1. In each case, the `Key` can be uniquely determined.

**Table 26.4-1. Key Generated Based on KeyA**

| BlockA     | Key         | Key Length (bit) |
|------------|-------------|------------------|
| Exists     | KeyA        | 256              |
| Does not exist | `0^256`    | 256              |

**Notes:**
*   `"0^256"` indicates a bit string that consists of 256-bit zeros.
*   Using `0^256` as `Key` is not secure. It is recommended to configure a valid key.

For more information of key purposes, please refer to Table 5.3-2 Secure Key Purpose Values in Chapter 5 eFuse Controller (EFUSE).

## 26.4.3 Target Memory Space

The target memory space refers to a continuous address space in the external memory (flash) where the ciphertext is stored. The target memory space can be uniquely determined by two relevant parameters: size and base address, whose definitions are listed below.

*   **Size**: the size of the target memory space, indicating the number of bytes encrypted in one encryption operation, which supports 16, 32, or 64 bytes.
*   **Base address**: the `base_addr` of the target memory space. It is a 24-bit physical address, with range of `0x0000_0000 ~ 0x00FF_FFFF`. It should be aligned to `size`, i.e., `base_addr % size == 0`.

For example, if there are 16 bytes of instruction data that need to be encrypted and written to address `0x130 ~ 0x13F` in the external flash, then the target space is `0x130 ~ 0x13F`, size is 16 (bytes), and the base address is `0x130`.

The encryption of any length (must be multiples of 16 bytes) of plaintext instruction/data can be completed separately in multiple operations, and each operation has its individual target memory space and the relevant parameters.

For Auto Decryption blocks, these parameters are automatically determined by hardware. For Manual Encryption blocks, these parameters should be configured by users.

**Note:**
The “tweak” defined in Section Data units and tweaks of IEEE Std 1619-2007 is a 128-bit non-negative integer
```