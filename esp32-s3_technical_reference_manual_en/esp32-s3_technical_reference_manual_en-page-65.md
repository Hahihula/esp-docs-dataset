**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading and Subheading with Content:**

**1.7 Instruction Performance**

For processors designed based on a pipeline, it is ideal that CPU issues one instruction onto the pipeline per processor cycle. The ESP32-S3 Xtensa processor adopts the 5-stage pipeline technology: I (instruction fetch), R (decode), E (execute), M (memory access), and W (write back). Table 1.7-1 shows what the processor does at each pipeline stage.

**Table Title:** 
Table 1.7-1. Five-Stage Pipeline of Xtensa Processor

| Pipeline Stage | Number | Operation |
|----------------|--------|-----------|
| I              | -      | Align instructions (24-bit and 32-bit instructions supported) |
| R              | 0      | Read the general-purpose registers AR and QR |
|                 |        | Decode instructions, detect interlocks, and forward operands |
| E              | 1      | For arithmetic instructions, the ALU (addition, subtraction, multiplication, etc.) works |
|                 |        | For read memory instructions, generate virtual addresses for memory access |
| M              | 2      | For branch jump instructions, select jump addresses |
| W              | 3      | Write back to registers the calculated results and the data read from memory |

The processor cannot issue an instruction to the pipeline until all the operands and hardware resources required for the operation are ready. However, there are following hazards in the actual program running process, which can cause stopped pipeline and delayed implementation of instructions.

**Subsection Heading:**
1.7.1 Data Hazard

When instruction A writes the result to register X (including explicit general-purpose registers and implicit special registers), and instruction B needs to use the same register as an input operand, this case is referred to as that instruction B depends on instruction A. If instruction A prepares the result to be written to register X at the end of the SA pipeline stage, and instruction B reads the data in register X at the beginning of the SB pipeline stage, then instruction A must be issued D=max(SA+SB-1, 0) cycles before instruction B.

If the processor fetches instruction B less than D cycles after instruction A, the processor delays issuing instruction B until D cycles have passed. The act of a processor delaying an instruction because of pipeline interactions is called an interlock.

Suppose the SA pipeline stage of instruction A is W and the SB pipeline stage of instruction B is E, instruction B is issued to the pipeline D=max(2-1+1, 0)=2 cycles later than instruction A as shown in Figure 1.7-1.
When the output operand of an instruction is designed to be available at the end of a pipeline stage, it means that the operation of the instruction over. Usually, instructions that depend on this result data must wait until the output operand is written to the corresponding register before retrieving it from the corresponding register.

The Xtensa processor supports the "bypass" operation. It detects when the input operand of an instruction is generated at which pipeline stage of the instruction and does not need to wait for the data to be written to the register. It can directly forward the data from the pipeline stage where it is needed.


**Footer:**
Espressif Systems  
65  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)