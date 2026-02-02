**Chapter Title:**
Chapter 14 AES Accelerator (AES)

**Section Titles and Descriptions with Details:**

- **Register 14.4. AES_KEY_n_REG (n: 0-7) (0x10+4*n):**
  - Description:
    - `AES_KEY_n_REG`: AES key material register.
    - Access Mode: Read/Write
    - Address Range: 0x00000000 to 0x00000007

- **Register 14.5. AES_TEXT_m_REG (m: 0-3) (0x30+4*m):**
  - Description:
    - `AES_TEXT_m_REG`: Plaintext and ciphertext register.
    - Access Mode: Read/Write
    - Address Range: 0x00000000 to 0x00000007

- **Register 14.6. AES_ENDIAN_REG (0x040):**
  - Description:
    - `AES_ENDIAN_REG`: Endianness selection register.
    - Access Mode: Read/Write
    - Address Range: 0x00000000 to 0x00000007

**Table for AES_ENDIAN:**

| Bit | Description |
|-----|-------------|
| 6   | Reserved (not used) |
| 5   | Endianness selection bit. |
| 4-3 | Reserved or not specified in the provided text snippet. |
| 2   | Reserved or not specified in the provided text snippet. |
| 1   | Reserved or not specified in the provided text snippet. |
| 0   | Reserved (not used) |

**Footer:**
- Page Number and Document Information:
  - "Espressif Systems"
  - "ESP32 TRM (Version 5.6)"
  - "Submit Documentation Feedback"