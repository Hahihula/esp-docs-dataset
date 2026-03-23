

```markdown
## Key Endianness

In Typical AES working mode, when filling key into `AES_KEY_m_REG` registers, users should follow the key endianness type specified in Table 19.4-3 and Table 19.4-4.

### Table 19.4-3. Key Endianness Type for AES-128 Encryption and Decryption

| Bit¹ | w[0]                          | w[1]                          | w[2]                          | w[3]²                         |
|------|--------------------------------|--------------------------------|--------------------------------|-------------------------------|
| [31:24]| `AES_KEY_0_REG[7:0]`          | `AES_KEY_1_REG[7:0]`           | `AES_KEY_2_REG[7:0]`           | `AES_KEY_3_REG[7:0]`          |
| [23:16]| `AES_KEY_0_REG[15:8]`         | `AES_KEY_1_REG[15:8]`          | `AES_KEY_2_REG[15:8]`          | `AES_KEY_3_REG[15:8]`         |
| [15:8]| `AES_KEY_0_REG[23:16]`        | `AES_KEY_1_REG[23:16]`         | `AES_KEY_2_REG[23:16]`         | `AES_KEY_3_REG[23:16]`        |
| [7:0]| `AES_KEY_0_REG[31:24]`        | `AES_KEY_1_REG[31:24]`         | `AES_KEY_2_REG[31:24]`         | `AES_KEY_3_REG[31:24]`        |

¹ Column “Bit” specifies the bytes of each word stored in w[0] ~ w[3].
² w[0] ~ w[3] are “the first Nk words of the expanded key” as specified in Section 5.2 Key Expansion in [NIST FIPS 197](#).

### Table 19.4-4. Key Endianness Type for AES-256 Encryption and Decryption

| Bit¹ | w[0]                          | w[1]                          | w[2]                          | w[3]                          | w[4]                          | w[5]                          | w[6]                          | w[7]²                         |
|------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|-------------------------------|
| [31:24]| `AES_KEY_0_REG[7:0]`          | `AES_KEY_1_REG[7:0]`           | `AES_KEY_2_REG[7:0]`           | `AES_KEY_3_REG[7:0]`           | `AES_KEY_4_REG[7:0]`           | `AES_KEY_5_REG[7:0]`           | `AES_KEY_6_REG[7:0]`           | `AES_KEY_7_REG[7:0]`          |
| [23:16]| `AES_KEY_0_REG[15:8]`         | `AES_KEY_1_REG[15:8]`          | `AES_KEY_2_REG[15:8]`          | `AES_KEY_3_REG[15:8]`          | `AES_KEY_4_REG[15:8]`          | `AES_KEY_5_REG[15:8]`          | `AES_KEY_6_REG[15:8]`          | `AES_KEY_7_REG[15:8]`         |
| [15:8]| `AES_KEY_0_REG[23:16]`        | `AES_KEY_1_REG[23:16]`         | `AES_KEY_2_REG[23:16]`         | `AES_KEY_3_REG[23:16]`         | `AES_KEY_4_REG[23:16]`         | `AES_KEY_5_REG[23:16]`         | `AES_KEY_6_REG[23:16]`         | `AES_KEY_7_REG[23:16]`        |
| [7:0]| `AES_KEY_0_REG[31:24]`        | `AES_KEY_1_REG[31:24]`         | `AES_KEY_2_REG[31:24]`         | `AES_KEY_3_REG[31:24]`         | `AES_KEY_4_REG[31:24]`         | `AES_KEY_5_REG[31:24]`         | `AES_KEY_6_REG[31:24]`         | `AES_KEY_7_REG[31:24]`        |

¹ Column “Bit” specifies the bytes of each word stored in w[0] ~ w[7].
² w[0] ~ w[7] are “the first Nk words of the expanded key” as specified in Chapter 5.2 Key Expansion in [NIST FIPS 197](#).
```