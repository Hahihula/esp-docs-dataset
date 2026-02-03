**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Heading:**
2.5 ULP-FSM

**Subsection and Content:**

#### Subsection Header:
2.5.1 Features

**Body Text:**
ULP-FSM is a programmable finite state machine that can work while the main CPU is in Deep-sleep. ULP-FSM supports instructions for complex logic and arithmetic operations, and also provides dedicated instructions for RTC controllers or peripherals. ULP-FSM can access up to 8 KB of SRAM RTC slow memory (accessible by the CPU) for instructions and data. Hence, such memory is usually used to store instructions and share data between the ULP coprocessor and the CPU. ULP-FSM can be stopped by running HALT instruction.

ULP-FSM has the following features:
- Provides four 16-bit general-purpose registers (RO, R1, R2, and R3) for manipulating data and accessing memory.
- Provides one 8-bit stage count register (Stage_cnt) which can be manipulated by ALU and used in JUMP instructions.
- Supports built-in instructions specially for direct control of low-power peripherals, such as SAR ADC and temperature sensor.

#### Subsection Header:
2.5.2 Instruction Set

**Body Text:**
ULP-FSM supports the following instructions:

- ALU: perform arithmetic and logic operations
- LD, ST, REG_RD and REG_WR: load and store data
- JUMP: jump to a certain address
- WAIT/HALT: manage program execution
- WAKE: wake up CPU or communicate with CPU
- TSENS and ADC: take measurements

**Figure Caption (below the list):**
Figure 2.5-1 shows the format of ULP-FSM instructions.

**Figure Description:**
Figure caption for Figure 2.5-1:
Figure 2.5-1. ULP-FSM Instruction Format
An instruction, which has one OpCode, can perform various operations, depending on the setting of Operands bits. A good example is the ALU instruction, which is able to perform 10 arithmetic and logic operations; or the JUMP instruction, which may be conditional or unconditional, absolute or relative.

Each instruction has a fixed width of 32 bits. A series of instructions can make a program be executed by the coprocessor. The execution flow inside the program uses 32-bit addressing. The program is stored in a dedicated region called Slow Memory, which is visible to the main CPU under an address range of 0x5000_0000 to 0x5000_1FFF (8 KB).

**Footer:**
Espressif Systems
310 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback