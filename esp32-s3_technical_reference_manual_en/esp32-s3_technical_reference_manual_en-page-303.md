**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.220 MV.QR

**Subsection - Instruction Word Table:**
- `Instruction Word`: 
  - `10`
  - `qu[2:1]` : `1111`
  - `qu[0]`   : `000`
  - `OOO`     : `000`
  - `qs[2:1]` : `000`
  - `qs[0]`   : `00100`

**Subsection - Assembler Syntax:**
- **MV.QR qu, qs**

**Subsection - Description:**
This instruction moves the value from the source QR register qs to the target QR register qu.

**Subsection - Operation:**
```
qu = qs
```