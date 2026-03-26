

```markdown
## 32.4.1 XTS Algorithm

The manual encryption and auto encryption/decryption all use the same algorithm. During implementation, the XTS algorithm is characterized by a "data unit" of 1024 bits, defined in the Section XTS-AES encryption procedure of

[XTS-AES Tweakable Block Cipher Standard](#). For more information about the XTS-AES algorithm, please refer to IEEE Std 1619-2007.

## 32.4.2 Key

The Manual Encryption block, Auto Encryption block, and Auto Decryption block share the same `Key` when implementing the XTS algorithm. The `Key` is provided by the eFuse hardware and cannot be accessed by users.

The `Key` can be either 256-bit or 512-bit long. The value and length of the `Key` are determined by the content in the eFuse blocks from Block4 ~ Block9 and corresponding eFuse parameters. For easier description, we define:

*   `Block_A`: the block whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_256_KEY_1 (please refer to Table 8.3-2 Secure Key Purpose Values). If `Block_A` exists, a 256-bit `Key_A` is stored in it.
*   `Block_B`: the block whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_256_KEY_2 (please refer to Table 8.3-2 Secure Key Purpose Values). If `Block_B` exists, a 256-bit `Key_B` is stored in it.
*   `Block_C`: the block whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_128_KEY (please refer to Table 8.3-2 Secure Key Purpose Values). If `Block_C` exists, a 256-bit `Key_C` is stored in it.

There are five possibilities of how the `Key` is generated depending on whether `Block_A`, `Block_B`, and `Block_C` exist or not, as shown in Table 32.4-1. In each case, the `Key` can be uniquely determined by `Block_A`, `Block_B` or `Block_C`.

Table 32.4-1. Key generated based on `Key_A`, `Key_B`, and `Key_C`

| Block_A | Block_B | Block_C | Key                         | Key Length (bit) |
|---------|---------|---------|------------------------------|------------------|
| Yes     | Yes     | Don't care | `Key_A || Key_B`             | 512              |
| Yes     | No      | Don't care | `Key_A || 0^256`             | 512              |
| No      | Yes     | Don't care | `0^256 || Key_B`             | 512              |
| No      | No      | Yes     | `Key_C`                      | 256              |
| No      | No      | No      | `0^256`                      | 256              |

**Notes:**

*   "YES" indicates that the block exists
*   "NO" indicates that the block does not exist
*   "0^256" indicates a bit string that consists of 256-bit zeros
*   "|" is a bonding operator for joining one-bit string to another

For more information on key purposes, please refer to Table 8.3-2 Secure Key Purpose Values in Chapter 8 eFuse Controller (EFUSE).
```