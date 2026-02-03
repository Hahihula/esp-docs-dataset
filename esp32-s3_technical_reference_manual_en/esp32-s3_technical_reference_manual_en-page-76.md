**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8 Extended Instruction Functional Description

**Body Text:**
Before reading this section, you are recommended to read the table [link] which introduces instruction field names and their meanings in instruction encoding.

[N:M] is used to represent the field. It means the width of the field is (N-M+1), namely, both bits N and M are included. For example, qa[2:0] has a total of 3 bits, which are bit0, bit1 and bit2, and qa[1] represents the value of bit1.

This chapter describes all the instructions mentioned in Section [link] in alphabetical order by the instruction name. Each instruction is encoded in little-endian bit order as shown in Figure [link].

**Subsection Header:**
1.8.1 EE.ANDQ

**Table Title: Instruction Word**

| 1 | qa[2:1] | 1101 | qa[0] | 011 | qy[2:1] | OO | qx[0] | 0100 |
|---|---------|------|-------|-----|---------|----|-------|------|
| **Assembler Syntax** | EE.ANDQ qa, qx, qy |

**Subsection Header:**
Description

**Body Text:**
This instruction performs a bitwise AND operation on registers qx and qy and writes the result of the logical operation to register qa.

**Subsection Header:**
Operation

**Body Text:**

1. qa = qx & qy