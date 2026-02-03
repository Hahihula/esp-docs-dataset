**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.17 EE.LD.128.USAR.IP

**Subsection - Instruction Word Table:**
- Columns labeled as `imm16[7]`, `qu[2:1]`, `0001`, `qu[0]`, `imm16[6:0]`, `as[3:0]`, and `0100`

**Subsection - Assembler Syntax:**
- Text reads "EE.LD.128.USAR.IP qu, as, -2048..2032"

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register `as` to zero and loads 16-byte data from memory to register `qu`. Meanwhile, it saves the value of the lower 4 bits in `as` into the special register `SAR_BYTE`. After the access is completed, the value in register `as` is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subsection - Operation:**
1. `qu[127:0] = load128({as[31:4],4{0}})`
2. `SAR_BYTE = as[3:0]`
3. `as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0], 4{0}}`

**Footer Information:**
- "Espressif Systems"
- Page number and document version information at the bottom right corner reads "93 ESP32-S3 TRM (Version 1.7)"
- Link labeled "Submit Documentation Feedback"