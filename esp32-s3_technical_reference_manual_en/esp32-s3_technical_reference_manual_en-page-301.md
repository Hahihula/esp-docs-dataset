**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.218 LD.QR

**Subheader - Instruction Word Breakdown Table:**
- `qu[2:1]`: 011, qu[0]
- `imm[3:0]`: 010
- `as[3:0]`: 0100

**Subheader - Assembler Syntax:**
LD.QR qu, as, imm, -128..112

**Subheader - Description:**
This instruction loads 128 bits from memory to the target QR register qu.

**Subheader - Operation (with code block):**
```
qu = load128(as + imm)
```