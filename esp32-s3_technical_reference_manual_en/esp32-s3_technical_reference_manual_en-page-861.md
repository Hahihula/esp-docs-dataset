**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Link:**
GoBack

**Table Title and Description:**
Table 19.4-3. Key Endianness Type for AES-128 Encryption and Decryption

| Bit | w[0] | w[1] | w[2] | w[3] |
|-----|------|------|------|------|
| [31:24] | AES_KEY_0_REG[7:0] | AES_KEY_1_REG[7:0] | AES_KEY_2_REG[7:0] | AES_KEY_3_REG[7:0] |
| [23:16] | AES_KEY_0_REG[15:8] | AES_KEY_1_REG[15:8] | AES_KEY_2_REG[15:8] | AES_KEY_3_REG[15:8] |
| [15:8] | AES_KEY_0_REG[23:16] | AES_KEY_1_REG[23:16] | AES_KEY_2_REG[23:16] | AES_KEY_3_REG[23:16] |
| [7:0] | AES_KEY_0_REG[31:24] | AES_KEY_1_REG[31:24] | AES_KEY_2_REG[31:24] | AES_KEY_3_REG[31:24] |

**Footnotes and References in Table:**
1. Column "Bit" specifies the bytes of each word stored in w[0] ~ w[3].
2. w[0] ~ w[3] are “the first Nk words of the expanded key” as specified in Section 5.2 Key Expansion in NIST FIPS 197.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)