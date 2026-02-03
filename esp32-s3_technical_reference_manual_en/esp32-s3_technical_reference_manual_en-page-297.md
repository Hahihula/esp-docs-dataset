**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.214 EE.XORQ

**Subsection - Instruction Word Table:**
- Columns are labeled as `qa[2:1]`, `qa[0]`, `qy[2:1]`, `qy[0]`, `qx[2:1]`, `qx[0]`, and `qy[0]`.
- Rows contain binary values (e.g., 11, 101).

**Subsection - Assembler Syntax:**
EE.XORQ qa, qx, qy

**Subsection - Description:**
This instruction performs a bitwise XOR operation on registers qx and qy and writes the result of the logical operation to register qa.

**Subsection - Operation Diagram (Markdown format):**
```
qa = qx ^ qy
```

**Footer Information:**
Espressif Systems, ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback