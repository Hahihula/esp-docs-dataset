**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.37 EE.LDXQ.32

**Subheader - Instruction Word Table:**
- sel4[1]
- sel8[0]
- sel11
- sel4[0]
- qu[2:0]
- qs[1:0]
- sel8[2:1]
- as[3:0]
- 111
- qs[2]

**Subheader - Assembler Syntax Description:**
EE.LDXQ.32 qu, qs, as, 0..3, 0..7

**Description Text:**
This instruction selects one of the 8 segments of 16-bit data in qs as the addend according to the immediate number sel8. It adds the operand left-shifted by 2 bits to the value of the address register as, uses the result as the access address, aligns it to 32 bits (its lower 2 bits are set to 0), and stores loaded data to a 32-bit data segment in register qu according to the value of the immediate number sel4.

**Subheader - Operation:**
1. vaddr[31:0] = as[31:0] + qs[ 15: 0] * 4
2. vaddr1[31:0] = as[31:0] + qs[ 31: 16] * 4
3. vaddr2[31:0] = as[31:0] + qs[ 47: 32] * 4
4. vaddr3[31:0] = as[31:0] + qs[ 63: 47] * 4
5. vaddr4[31:0] = as[31:0] + qs[ 79: 64] * 4
6. vaddr5[31:0] = as[31:0] + qs[ 95: 80] * 4
7. vaddr6[31:0] = as[31:0] + qs[111: 96] * 4
8. vaddr7[31:0] = as[31:0] + qs[127:112] * 4

9.
```
if sel8 == 0:
    dataIn[31:0] = load32({vaddr0[31:2],2{0}})
if sel8 == 1:
    dataIn[31:0] = load32({vaddr1[31:2],2{0}})
if sel8 == 2:
    dataIn[31:0] = load32({vaddr2[31:2],2{0}})
if sel8 == 3:
    dataIn[31:0] = load32({vaddr3[31:2],2{0}})
if sel8 == 4:
    dataIn[31:0] = load32({vaddr4[31:2],2{0}})
if sel8 == 5:
    dataIn[31:0] = load32({vaddr5[31:2],2{0}})
if sel8 == 6:
    dataIn[31:0] = load32({vaddr6[31:2],2{0}})
if sel8 == 7:
    dataIn[31:0] = load32({vaddr7[31:2],2{0}})
```

**Final Operation Line:**
qu[32*sel4+31:32*sel4] = dataIn[31:0]

**Footer Information:**
Espressif Systems
Page 113 of ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback