**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**GoBack Link:** [GoBack](#)

---

### Section Header:
19.4.1 Key, Plaintext, and Ciphertext

**Body Text:**
The encryption or decryption key is stored in `AES_KEY_n_REG`, which is a set of eight 32-bit registers.

- For AES-128 encryption/decryption, the 128-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_3_REG`.
- For AES-256 encryption/decryption, the 256-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_7_REG`.

The plaintext and ciphertext are stored in `AES_TEXT_IN_m_REG` and `AES_TEXT_OUT_m_REG`, which are two sets of four 32-bit registers.

- For AES-128/AES-256 encryption, the `AES_TEXT_IN_m_REG` registers are initialized with plaintext. Then, the AES Accelerator stores the ciphertext into `AES_TEXT_OUT_m_REG` after operation.
- For AES-128/AES-256 decryption, the `AES_TEXT_IN_m_REG` registers are initialized with ciphertext. Then, the AES Accelerator restores the plaintext into `AES_TEXT_OUT_m_REG` after operation.

---

### Section Header:
19.4.2 Endianness

**Subsection Title:**
Text Endianness

**Body Text:**
In Typical AES working mode, the AES Accelerator uses cryptographic keys to encrypt and decrypt data in blocks of 128 bits. When filling data into `AES_TEXT_IN_m_REG` register or reading result from `AES_TEXT_OUT_m_REG` registers, users should follow the text endianness type specified in Table 19.4-2.

**Table Title:**
Table 19.4-2. Text Endianness Type for Typical AES

| State | Plaintext/Ciphertext |
|-------|----------------------|
| c^0   | `AES_TEXT_x_0_REG[7:0]` | `AES_TEXT_x_1_REG[7:0]` | `AES_TEXT_x_2_REG[7:0]` | `AES_TEXT_x_3_REG[7:0]` |
| 1     | `AES_TEXT_x_0_REG[15:8]` | `AES_TEXT_x_1_REG[15:8]` | `AES_TEXT_x_2_REG[15:8]` | `AES_TEXT_x_3_REG[15:8]` |
| 2     | `AES_TEXT_x_0_REG[23:16]` | `AES_TEXT_x_1_REG[23:16]` | `AES_TEXT_x_2_REG[23:16]` | `AES_TEXT_x_3_REG[23:16]` |
| 3     | `AES_TEXT_x_0_REG[31:24]` | `AES_TEXT_x_1_REG[31:24]` | `AES_TEXT_x_2_REG[31:24]` | `AES_TEXT_x_3_REG[31:24]` |

**Footnote 1:** The definition of “State (including c and r)” is described in Section 3.4 The State in NIST FIPS 197.

**Footnote 2:** Where x = IN or OUT.

---

### Subsection Title:
Key Endianness

**Body Text:**
In Typical AES working mode, When filling key into `AES_KEY_m_REG` registers, users should follow the key endianness type specified in Table 19.4-3 and Table 19.4-4.

---

**Footer Information:** 
Espressif Systems  
Submit Documentation Feedback

**Document Version:**
ESP32-S3 TRM (Version 1.7)