**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.49 EE.SRC.Q

**Subsection - Instruction Word Table:**
- 11 | qs1[2:1] | 100 | qs1[0] | qs0[2:0] | 00110 | qa[2:0] | 0100

**Subsection Title:**
Assembler Syntax

**Body Text - Description:**
This instruction performs an arithmetic right shift on the 32-byte concatenation of registers qs0 and qs1 that hold the loaded data of two consecutive aligned addresses. By this way, you can obtain unaligned 16-byte data, which will be written to register qa. The right shift amount is SAR_BYTE multiplied by 8.

**Subsection Title:**
Operation

**Body Text - Operation Example:**
qa[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback