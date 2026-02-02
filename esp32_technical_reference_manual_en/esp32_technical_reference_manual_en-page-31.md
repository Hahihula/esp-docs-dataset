**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Subtitles and Sections with Content:**

- **Wake up/communicate with SoC - WAKE**
  
- **Take measurements - ADC**
  
- **Communicate using I2C - I2C_RD/I2C_WR**

**Figure Title:** Figure 1.4-1. The ULP Coprocessor Instruction Format

**Body Text:**
The ULP coprocessor’s instruction format is shown in [Figure 1.4-1](#).

An instruction, which has one OpCode, can perform various different operations, depending on the setting of Operands bits. A good example is the ALU instruction, which is able to perform 10 arithmetic and logic operations; or the JUMP instruction, which may be conditional or unconditional, absolute or relative.

Each instruction has a fixed width of 32 bits. A series of instructions can make a program be executed by the ULP coprocessor. The execution flow inside the program uses 32-bit addressing. The program is stored in a dedicated region called Slow Memory (RTC_SLOW_MEM), which is visible to the main CPUs as one that has an address range from 0x5000_0000 to 0x5000_1FFF (8 KB).

The OpCode in this chapter is represented by 4'dx, where 4 stands for 4-bit width, 'd' is a decimal symbol, x stands for the value of OpCode (x: 0 ~ 15).

**Subsection Title:** 
1.4.1 ALU - Perform Arithmetic/Logic Operations

**Body Text under Subsection:**
The ALU (Arithmetic and Logic Unit) performs arithmetic and logic operations on values stored in ULP coprocessor registers, and on immediate values stored in the instruction itself.

The following operations are supported:

- Arithmetic: ADD and SUB
- Logic: bitwise logical AND and bitwise logical OR
- Bit shifting: LSH and RSH
- Moving data to register: MOVE
- Stage count register manipulation: STAGE_RST, STAGE_INC and STAGE_DEC

The ALU instruction, which has one OpCode, can perform various different arithmetic and logic operations, depending on the setting of the instruction’s bits [27:21] accordingly.

**Subsection Title:** 
1.4.1.1 Operations Among Registers

**Body Text under Subsection:**
When bits {27:25} of the instruction in Figure 1.4-2 are set to 3'bO, ALU performs operations, using the ULP coprocessor register R[0-3]. The types of operations depend on the setting of the instruction’s bits [24:21] presented in Table 1.4-1.

**Figure Title:** Figure 1.4-2. Instruction Type — ALU for Operations Among Registers

**Table Description (from image):**
The table shows the relationship between OpCode and ALU operation types, with columns labeled OpCode bits from most significant to least significant bit: 31, 28, 27, etc., down to 0.

**Footer Text:** 
Espressif Systems  
ESP32 TRM (Version 5.6)  
[Submit Documentation Feedback](#)

(Note: The actual table content is not transcribed due to the image format and complexity.)