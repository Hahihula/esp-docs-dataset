**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.42 EE.MOV1.32.A

**Instruction Word Table:**
- 11 qs[2:1]
- 1101 qs[0]
- 111 sel4[1:0]
- 01 au[3:0]
- 0100

**Subheading - Assembler Syntax:**
EE.MOV1.32.A qs, au, 0..3

**Subheading - Description:**
This instruction selects one data segment of 32 bits from register qs according to immediate number sel4 and assigns it to register au.

**Subheading - Operation (with code block):**

```
if sel4 == 0:
    au = qs[ 31: ]
if sel4 == 1:
    au = qs[ 63: 32]
if sel4 == 2:
    au = qs[ 95: 64]
if sel4 == 3:
    au = qs[127: 96]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback