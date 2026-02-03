**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.95 EE.VLDBEC.16.IP

**Subsection - Instruction Word:**
```
10   qu[2:1]  0101   qu[0]   imm2[6:0]   as[3:0]   0100
```

**Subsection - Assembler Syntax:**
EE.VLDBEC.16.IP qu, as, 0..254

**Subsection - Description:**
This instruction forces the lower 1 bit of the access address in register `as` to 0, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register `qu`. After the access is completed, the value in register `as` is incremented by 7-bit unsigned-extended constant in the instruction code segment left-shifted by

**Subsection - Operation:**
```
1.   qu[127:0] = {8load16({as[31:1],1{0}})}
2.   as[31:0] = as[31:0] + {24{0},imm2[6:0],0}
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback