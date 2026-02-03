**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.98 EE.VLDBEC.32.IP

**Subsection Titles and Content:**

- **Instruction Word Table:**
  - `imm4[7]`
  - `qu[2:1]`
  - `0010`
  - `qu[0]`
  - `imm4[6:0]`
  - `as[3:0]`
  - `0100`

- **Assembler Syntax**
  - EE.VLDBEC.32.IP qu, as, -256..252

- **Description**
  - This instruction forces the lower two bits of the access address in register as to zero and loads 32-bit data from memory and broadcasts it to the four 32-bit data segments in register qu. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 2.

- **Operation**
  - `qu[127:0] = {4load32({as[31:2],2{0}})}`
  - `as[31:0] = as[31:0] + {22imm4[7]}, imm4[7:0], 2{0}`

**Footer Information:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback