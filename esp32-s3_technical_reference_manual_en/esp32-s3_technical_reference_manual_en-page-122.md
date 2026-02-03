**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.46 EE.SET_BIT_GPIO_OUT

**Subsection - Instruction Word:**
- Binary representation of the instruction word is shown as `01101010100 imm256[7:0] 0100`

**Subsection - Assembler Syntax:**
```
EE.SET_BIT_GPIO_OUT 0..255
```

**Subsection - Description:**
It is a dedicated CPU GPIO instruction to set certain bits of GPIO_OUT. The assignment content depends on the 8-bit immediate number imm256.

**Subsection - Operation:**
```
GPIO_OUT[7:0] = (GPIO_OUT[7:0] | imm256[7:0])
```

**Footer Information:**
- Page Number: 122
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Link Texts:**
- GoBack
- Submit Documentation Feedback