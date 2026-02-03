**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.45 EE.ORQ

**Instruction Word Table:**
- 11
- qa[2:1] 1101
- qa[0]    111
- qy[2:1] 00
- qx[2:1] 
- qx[0]   0x0
- qx[0]   0100

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.ORQ qa, qx, qy

**Description Section:**
This instruction performs a bitwise OR operation on registers qx and qy and writes the result of the logical operation to register qa.

**Operation Section:**
```
qa = qx | qy
```