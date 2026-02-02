**Title: Chapter 16 SHA Accelerator (SHA)**

**GoBack**

**Register Information Section**
- **Register Name:** Register 16.14, SHA_SHA512_START_REG (0x0B0)
  - **Description:** Write 1 to start an SHA-512 operation on the first message block.
  - **Access Mode:** WO
  - **Bit Fields:**
    - **SHA_SHASIZ_START**  
      - **Value:** 31
      - **Reset Value:** (reserved)
      - **Bits:** [0, 1]
- **Register Name:** Register 16.15, SHA_SHA512_CONTINUE_REG (0x0B4)
  - **Description:** Write 1 to continue the SHA-512 operation with subsequent blocks.
  - **Access Mode:** WO
  - **Bit Fields:**
    - **SHA_SHASIZ_CONTINUE**  
      - **Value:** 31
      - **Reset Value:** (reserved)
      - **Bits:** [0, 1]
- **Register Name:** Register 16.16, SHA_SHA512_LOAD_REG (0x0B8)
  - **Description:** Write 1 to finish the SHA-512 operation to calculate the final message hash.
  - **Access Mode:** WO
  - **Bit Fields:**
    - **SHA_SHASIZ_LOAD**  
      - **Value:** 31
      - **Reset Value:** (reserved)
      - **Bits:** [0, 1]

**Footer Information**
- Company Name: Espressif Systems
- Document Version and Type: ESP32 TRM (Version 5.6) 
- Page Number: 301

**Link Texts:**
- Submit Documentation Feedback