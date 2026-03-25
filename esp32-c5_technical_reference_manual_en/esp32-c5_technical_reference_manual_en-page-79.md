

```markdown
## 2.6 RISC-V Standard ISA Extensions Support

HP CPU core implements mandatory base integer ISA and is compliant with version 2.0 of RV32I base integer instruction set specified in RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2

### 2.6.1 Multiplication/Division (M) Extension

#### 2.6.1.1 Overview

In addition to the base RV32I instruction set, the HP core also implements standard integer multiplication and division extension and is fully compliant with version 2.0 of the standard extension "M" specified in the RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2.

#### 2.6.1.2 Functional Description

Instructions specified in "M" extension perform multiply and divide operations on the values held in two integer registers. Below are CPU cycle details taken by multiply and divide instructions in the absence of any data hazard in the pipeline.

*   MUL operation takes 2 cycles
*   DIV operation takes 1-19 cycles depending on operands

### 2.6.2 Compressed (C) Extension

#### 2.6.2.1 Overview

HP core also implements the RISC-V standard compressed instruction set extension named "C" and is fully compliant with version 2.0 of the standard extension "C" specified in RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2. RVC is a generic term used to specify C extension support. RVC reduces static and dynamic code size by adding short 16-bit instruction encoding for common operations. Typically, 50-60% of the RISC-V instructions in a program can be replaced with RVC instructions, resulting in a 25-35% code-size reduction.

#### 2.6.2.2 Functional Description

RVC uses a simple compression scheme that offers a shorter 16-bit version of 32-bit RISC-V instructions for any of the following scenarios:

1.  Immediate and address offset is small
2.  One of the registers is a zero register (x0), the ABI link register (x1), or the ABI stack pointer (x2)
3.  Destination register and the first source register are identical, or
4.  The registers used are the 8 most popular ones i.e., x8-x15.
```