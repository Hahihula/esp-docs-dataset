**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header and Subsection with Code Example:**
1.5.1 General-Purpose Registers

When using general-purpose register as operands in instructions, you need to explicitly declare the number of the assigned register.

Example:
```
EE.VADDS.S8 q2, q0, q1
```

This instruction uses No.0 and No.1 QR registers as input vectors and stores the vector addition result in the No.2 QR register.

**Subsection: AR**
Each AR register operand in the instruction will occupy a 4-bit code length. You can select any of the 16 AR registers as operands, and the 4-bit code value indicates the number to declare. The row "a*" in table 1.4-1 lists various purposes of AR registers in the extended instruction set, including address storage and data storage.

**Subsection: FR**
Each FR register operand in the instruction will occupy a 4-bit code length. You can select any of the 16 FR registers as operands, and the 4-bit code value indicates the number to declare. In ESP32-S3 extended instruction set, there are only read and write instructions for floating-point data. They are 4 times more efficient than the 32-bit floating-point data R/W instructions that are native to the Xtensa processor, thanks to the 128-bit access bandwidth.

**Subsection: QR**
In order to improve the execution efficiency of the program, operands are usually stored in general-purpose registers to save time spent in reading from memory. The AR registers native to Xtensa only have 32-bit width, while ESP32-S3 can access 128-bit data at a time, so they can only use 1/4 bandwidth capacity of the existing data bus. For this reason, ESP32-S3 has added eight 128-bit customized general-purpose registers, i.e., QR registers. QR registers are mainly used to store the data acquired/used by the 128-bit data bus to read or write memory, as well as to temporarily store the operation results generated from 128-bit data operations.

As the processor executes instructions, an individual QR register is treated as 16 8-bit or 8 16-bit or 4 32-bit operands depending on the vector operation bit width defined by the instruction, thus enabling a single instruction to perform operations on multiple operands.

**Subsection: Special Registers**
Different from general-purpose registers, special registers are implicitly called in specific instructions. You do not need to and cannot specify a certain special register when executing instructions. For example:

Example:
```
EE.VMUL.S16 q2, q0, q1
```

This vector multiplication instruction uses q0 and q1 general-purpose registers as inputs. During the internal operation, the intermediate 32-bit multiplication result is shifted to the right, and then the lower 16-bit of the result is retained to form a 128-bit output to q2. The shift amount in the process is determined by the value in the Shift Amount Register (SAR) and this SAR register will not appear in the instruction operand list.

**Footer:**
Espressif Systems
46 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback