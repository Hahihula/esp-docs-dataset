**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.69 EE.STXQ.32

**Instruction Word Table:**
- 110011 sel[4] | sel[8]0 qv [2:0] sel[4][0] qs[1:0] sel[8][2:1] 000 as[3:0] 111 qs[2]

**Subsection Title:**
Assembler Syntax

**Syntax Description:**
EE.STXQ.32 qv, qs, as, sel4, sel8

**Description Section:**
This instruction selects one of the four data segments of 32 bits in register qv according to immediate number sel4. Then it selects an addend from the 8 data segments of 16 bits in register qs according to immediate number sel8, adds the addend left-shifted by 2 bits to the value of the address register as, aligns the sum to 32 bits (its lower 2 bits are set to 0), and uses the result as the written address.

**Operation Section:**
- vaddr[31:0] = as[31:0] + qs[ 15: ] * 4
- vaddr1[31:0] = as[31:0] + qs[ 31: 16 ] * 4
- vaddr2[31:0] = as[31:0] + qs[ 47: 32 ] * 4
- vaddr3[31:0] = as[31:0] + qs[ 63: 47 ] * 4
- vaddr4[31:0] = as[31:0] + qs[ 79: 64 ] * 4
- vaddr5[31:0] = as[31:0] + qs[ 95: 80 ] * 4
- vaddr6[31:0] = as[31:0] + qs[111: 96 ] * 4
- vaddr7[31:0] = as[127:112] * 4

**Conditional Operations Section (with code):**
```
if sel8 == 0:
    qv[32*sel4+31:32*sel4] =>store32({vaddr0[31:2],2{0}})
if sel8 == 1:
    qv[32*sel4+31:32*sel4] =>store32({vaddr1[31:2],2{0}})
if sel8 == 2:
    qv[32*sel4+31:32*sel4] =>store32({vaddr2[31:2],2{0}})
if sel8 == 3:
    qv[32*sel4+31:32*sel4] =>store32({vaddr3[31:2],2{0}})
if sel8 == 4:
    qv[32*sel4+31:32*sel4] =>store32({vaddr4[31:2],2{0}})
if sel8 == 5:
    qv[32*sel4+31:32*sel4] =>store32({vaddr5[31:2],2{0}})
if sel8 == 6:
    qv[32*sel4+31:32*sel4] =>store32({vaddr6[31:2],2{0}})
if sel8 == 7:
    qv[32*sel4+31:32*sel4] =>store32({vaddr7[31:2],2{0}})
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback