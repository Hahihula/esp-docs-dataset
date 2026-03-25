

```markdown
## 22.5.2 Endianness

### Text Endianness

In Typical AES working mode, the AES accelerator uses cryptographic keys to encrypt and decrypt data in blocks of 128 bits. When filling data into `AES_TEXT_IN_m_REG` register or reading result from `AES_TEXT_OUT_m_REG` registers, users should follow the text endianness type specified in Table 22.5-2.

Table 22.5-2. Text Endianness Type for Typical AES

| State¹ | 0 | 1 | 2 | 3 |
|--------|---|---|---|---|
| [r]    | `AES_TEXT_x_O_REG[7:0]`<br>`AES_TEXT_x_O_REG[15:8]`<br>`AES_TEXT_x_O_REG[23:16]`<br>`AES_TEXT_x_O_REG[31:24]` | `AES_TEXT_x_1_REG[7:0]`<br>`AES_TEXT_x_1_REG[15:8]`<br>`AES_TEXT_x_1_REG[23:16]`<br>`AES_TEXT_x_1_REG[31:24]` | `AES_TEXT_x_2_REG[7:0]`<br>`AES_TEXT_x_2_REG[15:8]`<br>`AES_TEXT_x_2_REG[23:16]`<br>`AES_TEXT_x_2_REG[31:24]` | `AES_TEXT_x_3_REG[7:0]`<br>`AES_TEXT_x_3_REG[15:8]`<br>`AES_TEXT_x_3_REG[23:16]`<br>`AES_TEXT_x_3_REG[31:24]` |

¹ The definition of "State (including c and r)" is described in Section 3.4 The State in NIST FIPS 197.
² Where `x = IN or OUT`.
```