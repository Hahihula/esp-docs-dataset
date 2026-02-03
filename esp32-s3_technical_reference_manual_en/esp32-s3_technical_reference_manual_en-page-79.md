**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.3 EE.CLK_BIT_GPIO_OUT

**Instruction Word:**
01101100100 imm256[7:0] 0100

**Assembler Syntax:**
EE.CLK_BIT_GPIO_OUT 0..255

**Description:**
It is a dedicated CPU GPIO instruction to clear certain GPIO_OUT bits. The content to clear depends on the 8-bit immediate number imm256.

**Operation:**
GPIO_OUT[7:0] = (GPIO_OUT[7:0] & ~imm256[7:0])

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback