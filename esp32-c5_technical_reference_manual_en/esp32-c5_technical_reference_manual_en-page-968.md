

```markdown
## 29.4.1 XTS Algorithm

Both manual encryption and auto encryption/decryption use the XTS algorithm. During implementation, the XTS algorithm is characterized by a "data unit" of 1024 bits, defined in the Section XTS-AES encryption procedure of XTS-AES Tweakable Block Cipher Standard. For more information about the XTS-AES algorithm, please refer to IEEE Std 1619-2007.

## 29.4.2 Key

The Manual Encryption block, Auto Encryption block, and Auto Decryption block share the same `Key` when implementing the XTS algorithm. The `Key` is provided by the eFuse hardware and cannot be accessed by software.

The `Key` is 256-bit long. The value of the `Key` is determined by the content in one eFuse block from BLOCK4 ~ BLOCK9. For easier description, we define:

*   `Block_A`: the block whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_128_KEY (please refer to Table 7.3-2 Secure Key Purpose Values) in Chapter 7 eFuse Controller (EFUSE). If `Block_A` exists, a 256-bit `Key_A` is stored in it.

There are two possibilities of how the `Key` is generated depending on whether `Block_A` exists or not, as shown in Table 29.4-1. In each case, the `Key` can be uniquely determined.

Table 29.4-1. Key Generated Based on `Key_A`

| Block_A | Key   | Key Length (bit) |
|---------|-------|------------------|
| Exists  | `Key_A` | 256             |
| Does not exist | `0^256` | 256             |

**Notes:**

*   `"0^256"` indicates a bit string that consists of 256-bit zeros.
*   Using `0^256` as `Key` is not secure. It is recommended to configure a valid key.

For more information of key purposes, please refer to Table 7.3-2 Secure Key Purpose Values in Chapter 7 eFuse Controller (EFUSE).

## 29.4.3 Target Memory Space

The target memory space refers to a continuous address space in the external memory where the first encrypted ciphertext is stored. The target memory space can be uniquely determined by three relevant parameters: type, size, and base address, whose definitions are listed below.

*   **Type:** the `type` of the target memory space, either external flash or external RAM. Value 0 indicates external flash, while 1 indicates external RAM.
*   **Size:** the `size` of the target memory space, indicating the number of bytes encrypted in one encryption operation, which supports 16, 32, or 64 bytes.
*   **Base address:** the `base_addr` of the target memory space. It is a 24-bit physical address, with range of `0x0000_0000 ~ 0x00FF_FFFF`. It should be aligned to `size`, i.e., `base_addr % size == 0`.
```