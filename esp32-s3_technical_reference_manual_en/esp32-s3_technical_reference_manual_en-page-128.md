**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.52 EE.SRC.Q.QU

**Instruction Word Table:**
- 11 | qs1[2:1] | 1100 | qs1[0] | qs0[2:0] | 01110 | qa[2:0] | 0100

**Subsection Title:**
Assembler Syntax

**Syntax Line:**
EE.SRC.Q.QUOp qa, qs0, qs1

**Subsection Title:**
Description

**Body Text:**
This instruction performs an arithmetic right shift on the 32-byte concatenation of registers qs0 and qs1 that hold the loaded data of two consecutive aligned addresses. In this way, you can obtain unaligned 16-byte data, which will be written to register qa. The right shift amount is SAR_BYTE multiplied by 8. At the same time, the value of register qs1 is updated to qs0.

**Subsection Title:**
Operation

**Body Text with Code Block:**
```
qa[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}
qs0 = qs1
```

**Footer Information:**
Espressif Systems

**Page Number and Document Version:**
128 ESP32-S3 TRM (Version 1.7)

**Link Texts:**
Submit Documentation Feedback