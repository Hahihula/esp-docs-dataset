**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Table Header:**
Table 23.4-1 Key generated based on Key_A, Key_B and Key_C

| Block_A | Block_B | Block_C | Key | Key Length (bit) |
|---------|---------|---------|-----|------------------|
| Yes     | Yes     | Don't care | Key_A || Key_B  | 512   |
| Yes     | No      | Don't care | Key_A ||0^256    | 512   |
| No      | Yes     | Don't care | 0^256||Key_B   | 512   |
| No      | No      | Yes       | Key_C        | 256   |
| No      | No      | No       | 0^256       | 256   |

**Notes:**
"YES" indicates that the block exists; "NO" indicates that the block does not exist; "0^256" indicates a bit string that consists of 256-bit zeros; "||" is a bonding operator for joining one bit string to another.

For more information of key purposes, please refer to Table 5.3-2 Secure Key Purpose Values in Chapter 5 eFuse Controller.

**Section Title:**
23.4.3 Target Memory Space

**Body Text:**
The target memory space refers to a continuous address space in the external memory where the first encrypted ciphertext is stored. The target memory space can be uniquely determined by three relevant parameters: type, size and base address, whose definitions are listed below.

- **Type:** the `type` of the target memory space, either external flash or external RAM. Value 0 indicates external flash, while 1 indicates external RAM.
  
- **Size:** the `size` of the target memory space, indicating the number bytes encrypted in one encryption operation, which supports 16, 32 or 64 bytes.

- **Base address:** the `base_addr` of the target memory space. It is a 30-bit physical address, with range of 0x0000_0000 ~ 0x3FFF_FFFF. It should be aligned to `size`, i.e., `base_addr%size == 0`.

For example, if there are 16 bytes of instruction data need to be encrypted and written to address 0x130 ~ 0x13F in the external flash, then the target space is 0x130 ~ 0x13F, type is O (external flash), size is 16 (bytes), and base address is 0x130.

The encryption of any length (must be multiples of 16 bytes) of plaintext instruction/data can be completed separately in multiple operations, and each operation has individual target memory space and the relevant parameters.
For Auto Encryption/Decryption blocks, these parameters are automatically defined by hardware. For Manual Encryption block, these parameters should be configured manually by users.

**Note:**
The "tweak" defined in Chapter 5.1 Data units and tweaks of IEEE Std 1619-2007 is a 128-bit non-negative integer (`(tweak)`), which can be generated according to `tweak = type * 2^30 + (base_addr & 0x3FFFFF80)`. The lowest 7 bits and the highest 97 bits in `tweak` are always zero.

**Section Title:**
23.4.4 Data Padding

**Body Text:**
For Auto Encryption/Decryption blocks, data padding is automatically completed by hardware. For Manual Encryption block, data padding should be completed manually by users. The Manual Encryption block has a Espressif Systems 911 ESP32-S3 TRM (Version 1.7)

**Button:**
Submit Documentation Feedback