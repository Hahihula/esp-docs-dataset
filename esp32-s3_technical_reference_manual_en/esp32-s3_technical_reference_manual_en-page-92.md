**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.16 EE.GET_GPIO_IN

**Subsection - Instruction Word:**
- **Binary Representation:** `0110010100000100`
- **Hexadecimal Representation:** `au[3:0] 0100`

**Subsection - Assembler Syntax:**
```
EE.GET_GPIO_IN au
```

**Subsection - Description:**
It is a dedicated CPU GPIO instruction to assign the content of GPIO_IN to the lower 8 bits of register au.

**Subsection - Operation:**
```
au = {24'h0, GPIO_IN[7:0]}
```