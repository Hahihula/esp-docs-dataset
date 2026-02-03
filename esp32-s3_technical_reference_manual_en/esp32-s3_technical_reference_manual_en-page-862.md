Title: Key Endianness Type for AES-256 Encryption and Decryption

Table:
| Bit^1 | w[0]       | w[1]     | w[2]      | w[3]        | w[4]         | w[5]          | w[6]           | w[7]^2 |
|-------|------------|----------|-----------|-------------|--------------|---------------|----------------|--------|
| [31:24]| AES_KEY_0_REG[7:0] | AES_KEY_1_REG[7:0] | AES_KEY_2_REG[7:0] | AES_KEY_3_REG[7:0] | AES_KEY_4_REG[7:0] | AES_KEY_5_REG[7:0] | AES_KEY_6_REG[7:0] | AES_KEY_7_REG[7:0] |
| [23:16]| AES_KEY_0_REG[15:8] | AES_KEY_1_REG[15:8] | AES_KEY_2_REG[15:8] | AES_KEY_3_REG[15:8] | AES_KEY_4_REG[15:8] | AES_KEY_5_REG[15:8] | AES_KEY_6_REG[15:8] | AES_KEY_7_REG[15:8] |
| [15:8]| AES_KEY_0_REG[23:16] | AES_KEY_1_REG[23:16] | AES_KEY_2_REG[23:16] | AES_KEY_3_REG[23:16] | AES_KEY_4_REG[23:16] | AES_KEY_5_REG[23:16] | AES_KEY_6_REG[23:16] | AES_KEY_7_REG[23:16] |
| [7:0]| AES_KEY_0_REG[31:24] | AES_KEY_1_REG[31:24] | AES_KEY_2_REG[31:24] | AES_KEY_3_REG[31:24] | AES_KEY_4_REG[31:24] | AES_KEY_5_REG[31:24] | AES_KEY_6_REG[31:24] | AES_KEY_7_REG[31:24] |

Footnotes:
1. Column “Bit” specifies the bytes of each word stored in w[0] ~ w[7].
2. w[0] ~ w[7] are "the first Nk words of the expanded key" as specified in Chapter 5.2 Key Expansion in *NIST FIPS 197*.

Page Footer:
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback
- GoBack

Note: The image also contains a watermark or logo on the left side, but it is not described as per your instructions to focus only on text content and avoid any conversational elements that are outside of my capabilities based solely upon visible information in this document page provided by you.