**Chapter Title:**
Chapter 14 AES Accelerator (AES)

**Body Text:**
encryption/decryption, the 192-bit key is stored in AES_KEY_0_REG ~ AES_KEY_5_REG. For AES-256 encryption/decryption, the 256-bit key is stored in AES_KEY_0_REG ~ AES_KEY_7_REG.

Plaintext and ciphertext are stored in the AES_TEXT_m_REG registers. There are four 32-bit registers. To enable AES-128/192/256 encryption, initialize the AES_TEXT_m_REG registers with plaintext before encryption. When encryption is finished, the AES Accelerator will store back the resulting ciphertext in the AES_TEXT_m_REG registers. To enable AES-128/192/256 decryption, initialize the AES_TEXT_m_REG registers with ciphertext before decryption. When decryption is finished, the AES Accelerator will store back the resulting plaintext in the AES_TEXT_m_REG registers.

**Subsection Title:**
14.3.3 Endianness

**Subsection Subtitle (Key Endianness):**

Bit 0 and bit 1 in AES_ENDIAN_REG define the key endianness. For detailed information, please see Table 14.3-3 , Table 14.3-4 and Table 14.3-5 . w[0] ~ w[3] in Table 14.3-3 , w[0] ~ w[5] in Table 14.3-4 and w[0] ~ w[7] in Table 14.3-5 are “the first Nk words of the expanded key” as specified in “5.2: Key Expansion” of FIPS PUB 197, "Column Bit" specifies the bytes in the word from w[0] to w[7]. The bytes of AES_KEY_n_REG comprise “the first Nk words of the expanded key”.

**Subsection Subtitle (Text Endianness):**

Bit 2 and bit 3 in AES_ENDIAN_REG define the endianness of input text, while Bit 4 and Bit 5 define the endianness of output text. The input text refers to the plaintext in AES-128/192/256 encryption and the ciphertext in decryption. The output text refers to the ciphertext in AES-128/192/256 encryption and the plaintext in decryption. For details, please see Table 14.3-2 . “State” in Table 14.3-2 is defined as that in "3.4: The State" of FIPS PUB 197: “The AES algorithm operations are performed on a two-dimensional array of bytes called the State”. The ciphertext or plaintexts stored in each byte of AES_TEXT_m_REG comprise the State.

**Table Title and Content (Table 14.3-2):**

Title: Table 14.3-2 AES Text Endianness

| AES_ENDIAN_REG[3/5] | AES_ENDIAN_REG[2/4] | Plaintext/Ciphertext |
|---------------------|----------------------|----------------------|
| State               |                      |                     |
| 0                   | 0                    | AES_TEXT_3_REG(31:24) | AES_TEXT_2_REG(31:24) | AES_TEXT_1_REG(31:24) | AES_TEXT_0_REG(31:24) |
| 0                   | 1                    | AES_TEXT_3_REG(31:16) | AES_TEXT_2_REG(31:16) | AES_TEXT_1_REG(31:16) | AES_TEXT_0_REG(31:16) |
| 1                   | 0                    | AES_TEXT_3_REG(15:8)   | AES_TEXT_2_REG(15:8)    | AES_TEXT_1_REG(15:8)    | AES_TEXT_0_REG(15:8)    |
| 1                   | 1                    | AES_TEXT_3_REG(7:0)    | AES_TEXT_2_REG(7:0)     | AES_TEXT_1_REG(7:0)     | AES_TEXT_0_REG(7:0)     |

**Footer Text and Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Page number: 282

**Link Texts:**
GoBack, Submit Documentation Feedback