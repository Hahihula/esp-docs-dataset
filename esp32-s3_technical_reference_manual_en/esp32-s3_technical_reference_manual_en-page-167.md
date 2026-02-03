**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.91 EE.VLD.H.64.XP

**Subsection - Instruction Word:**
- `qu[2:1]`: 101, `qu[0]`: 110, `ad[3:0]`: 0100
- `as[3:0]`: (blank)

**Subsection - Assembler Syntax:**
```
EE.VLD.H.64.XP qu, as, ad
```

**Subsection - Description:**
This instruction forces the lower 3 bits of the access address in register `as` to 0 and loads 64-bit data from memory to the upper 64-bit segment in register `qu`. After the access is completed, the value in register `as` is incremented by the value in register `ad`.

**Subsection - Operation:**
```
1. qu[127: 64] = load64({as[31: 3],3{0}})
2. as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback