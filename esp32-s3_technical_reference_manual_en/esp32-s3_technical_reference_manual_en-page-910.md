**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Section Header with Link:**
GoBack

**Body Text:**
Section XTS-AES encryption procedure of XTS-AES Tweakable Block Cipher Standard. For more information about XTS-AES algorithm, please refer to [IEEE Std 1619-2007](http://www.ieee.org/standards/).

**Subsection Title and Number:**
23.4.2 Key

**Body Text with Description of Key Block:**
The Manual Encryption block, Auto Encryption block and Auto Decryption block share the same `Key` when implementing XTS algorithm. The `Key` is provided by the eFuse hardware and cannot be accessed by users.

The `Key` can be either 256-bit or 512-bit long. The value and length of the `Key` are determined by eFuse parameters. For easier description, now define:

- **Bullet Points:**
  - Block_A: the BLOCK in BLOCK4 ~ BLOCK9 whose key purpose is EFUSE_KEY_PURPOSE_XTS_AES_256_KEY_1. If Block_A is true, then the 256-bit `Key_A` is stored in it.
  - Block_B: the BLOCK in BLOCK4 ~ BLOCK9 whose key purpose is EFUSE_KEY PURPOSE_XTS_AES_256_KEY_2. If Block_B is true, then the 256-bit `Key_B` is stored in it.
  - Block_C: the BLOCK in BLOCK4 ~ BLOCK9 whose key purpose is EFUSE_KEY PURPOSE_XTS_AES_128_KEY. If Block_C is true, then the 256-bit `Key_C` is stored in it.

**Additional Information about Key Generation Possibilities:**
There are five possibilities of how the `Key` is generated depending on whether Block_A, Block_B and Block_C exists or not, as shown in Table **23.4-1**. In each case, the `Key` can be uniquely determined by Block_A, Block_B or Block_C.

**Footer:**
Espressif Systems
910 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback