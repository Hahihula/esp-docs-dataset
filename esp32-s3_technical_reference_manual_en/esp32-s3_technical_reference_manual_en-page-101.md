**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.25 EE.LDF.128.IP

**Subsection - Instruction Word Table:**
- `Instruction Word`
  - `10000 fu3[3:1] fu0[3:0] fu3[0] fu2[3:1] fu1[3:0] imm16f[3:0] as[3:0] 111 fu2[0]`

**Subsection - Assembler Syntax Table:**
- `Assembler Syntax`
  - `EE.LDF.128.IP fu3, fu2, fu1, fu0, os, -128..112`

**Subsection Title: Description**

**Body Text under "Description":**
This instruction forces the lower 4 bits of the access address in register as to zero, loads 16-byte data from memory, and stores it in order from low bit to high bit to floating-point registers fu0, fu1, fu2, and fu3. After the access is completed, the value in register as is incremented by 4-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subsection Title: Operation**

**Body Text under "Operation":**
```
dataIn[127:0] = load128({as[31:4],4{0}})
fu3 = dataIn[96]
fu2 = dataIn[95:64]
fu1 = dataIn[63:32]
fu0 = dataIn[ 31:   0 {24imm16f[3]},imm16f[3:0],4{0}}
as[31:0] = as[31:0]
```

**Footer Information:**
- "Espressif Systems"
- Page number and document version information at the bottom right corner:
  - `ESP32-S3 TRM (Version 1.7)`
- Link to submit documentation feedback.

**Navigation Links:**
- GoBack link in blue text on top-right side of page.
- Submit Documentation Feedback link below footer section, also highlighted as a hyperlink with underlined and bolded format "Submit Documentation Feedback".