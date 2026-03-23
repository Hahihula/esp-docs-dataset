
```markdown
## 19.4 Typical AES Working Mode

In the Typical AES working mode, users can check the working status of the AES accelerator by inquiring the `AES_STATE_REG` register and comparing the return value against the Table 19.4-1 below.

Table 19.4-1. Working Status under Typical AES Working Mode

| AES_STATE_REG | Status   | Description                                                                 |
|---------------|----------|-----------------------------------------------------------------------------|
| 0             | IDLE     | The AES accelerator is idle or completed operation.                         |
| 1             | WORK     | The AES accelerator is in the middle of an operation.                       |

### 19.4.1 Key, Plaintext, and Ciphertext

The encryption or decryption key is stored in `AES_KEY_n_REG`, which is a set of eight 32-bit registers.

*   For AES-128 encryption/decryption, the 128-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_3_REG`.
*   For AES-256 encryption/decryption, the 256-bit key is stored in `AES_KEY_0_REG ~ AES_KEY_7_REG`.

The plaintext and ciphertext are stored in `AES_TEXT_IN_m_REG` and `AES_TEXT_OUT_m_REG`, which are two sets of four 32-bit registers.

*   For AES-128/AES-256 encryption, the `AES_TEXT_IN_m_REG` registers are initialized with plaintext. Then, the AES accelerator stores the ciphertext into `AES_TEXT_OUT_m_REG` after operation.
*   For AES-128/AES-256 decryption, the `AES_TEXT_IN_m_REG` registers are initialized with ciphertext. Then, the AES accelerator stores the plaintext into `AES_TEXT_OUT_m_REG` after operation.

### 19.4.2 Endianness

#### Text Endianness

In Typical AES working mode, the AES accelerator uses cryptographic keys to encrypt and decrypt data in blocks of 128 bits. When filling data into `AES_TEXT_IN_m_REG` register or reading result from `AES_TEXT_OUT_m_REG` registers, users should follow the text endianness type specified in Table 19.4-2.

Table 19.4-2. Text Endianness Type for Typical AES

| State¹ | Plaintext/Ciphertext                                                                 |
|--------|--------------------------------------------------------------------------------------|
|        | c²                                                                                   |
|        | 0                               | 1                                 | 2                                 | 3                                 |
| 0      | `AES_TEXT_x_0_REG[7:0]`           | `AES_TEXT_x_1_REG[7:0]`           | `AES_TEXT_x_2_REG[7:0]`           | `AES_TEXT_x_3_REG[7:0]`           |
| r      | `AES_TEXT_x_0_REG[15:8]`          | `AES_TEXT_x_1_REG[15:8]`          | `AES_TEXT_x_2_REG[15:8]`          | `AES_TEXT_x_3_REG[15:8]`          |
|        | `AES_TEXT_x_0_REG[23:16]`         | `AES_TEXT_x_1_REG[23:16]`         | `AES_TEXT_x_2_REG[23:16]`         | `AES_TEXT_x_3_REG[23:16]`         |
|        | `AES_TEXT_x_0_REG[31:24]`         | `AES_TEXT_x_1_REG[31:24]`         | `AES_TEXT_x_2_REG[31:24]`         | `AES_TEXT_x_3_REG[31:24]`         |

¹ The definition of "State (including c and r)" is described in Section 3.4 The State in NIST FIPS 197.
² Where x = IN or OUT.
```