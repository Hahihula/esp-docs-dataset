**Chapter Title:**
Chapter 16 SHA Accelerator (SHA)

**Section Heading:**
16.5 Registers

**Body Text:**
The addresses in this section are relative to the SHA Accelerator base address provided in Table 3.3-6 in Chapter 3 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Subsection Title (with reference):**
Register 16.1. SHA_TEXT_n_REG (n: 0-31) (0x04+*n)

**Table Description for Subsection:**
- **Column Headers:** 
  - Address
  - Value

- **Rows:**
  - Row with address "31" and value "0x00000000"
    - SHA_TEXT_n_REG (n: 0-31) : SHA Message block and hash result register. (R/W)

**Subsection Title:** 
Register 16.2. SHA_SHA1_START_REG (0x080)

**Table Description for Subsection:**
- **Column Headers:** 
  - Address
  - Value

- **Rows:**
  - Row with address "31" and value "0x00000000"
    - SHA_SHA1_START: Write 1 to start an SHA-1 operation on the first message block. (WO)

**Subsection Title:** 
Register 16.3. SHA_SHA1_CONTINUE_REG (0x084)

**Table Description for Subsection:**
- **Column Headers:** 
  - Address
  - Value

- **Rows:**
  - Row with address "31" and value "0x00000000"
    - SHA_SHA1_CONTINUE: Write 1 to continue the SHA-1 operation with subsequent blocks. (WO)

**Subsection Title:** 
Register 16.4. SHA_SHA1_LOAD_REG (0x088)

**Table Description for Subsection:**
- **Column Headers:** 
  - Address
  - Value

- **Rows:**
  - Row with address "31" and value "0x00000000"
    - SHA_SHA1_LOAD: Write 1 to finish the SHA-1 operation to calculate the final message hash. (WO)

**Footer Information:** 
Espressif Systems
297 ESP32 TRM (Version 5.6)
Submit Documentation Feedback