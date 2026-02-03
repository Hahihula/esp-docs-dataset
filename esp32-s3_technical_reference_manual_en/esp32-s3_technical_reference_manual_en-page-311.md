**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Heading:**
2.5.2.1 ALU - Perform Arithmetic and Logic Operations

**Body Text:**
ALU (Arithmetic and Logic Unit) performs arithmetic and logic operations on values stored in ULP coprocessor registers, and on immediate values stored in the instruction itself. The following operations are supported.

- **Arithmetic:** ADD and SUB
- **Logic:** bitwise logical AND and bitwise logical OR
- **Bit shifting:** LSH and RSH
- **Moving data to register:** MOVE
- **PC register operations - STAGE_RST, STAGE_INC, and STAGE_DEC**

The ALU instruction, which has one OpCode (7), can perform various arithmetic and logic operations depending on the setting of the instruction bits [27:21].

**Subheading with Diagram Title:**
Operations Among Registers

**Diagram Description:**
Figure 2.5-2 shows an example where specific bits in a ULP-FSM register are set to zero, indicating that ALU performs certain types of operations on data stored within the registers.

**Table Caption and Content:**
When bits [27:26] of the instruction in Figure 2.5-2 are set to O, ALU performs operations on the data stored in ULP-FSM registers R[0-3]. The table below shows different types of operations depending on the setting of these instructions.

**Table Title and Content (Table 2.5-1):**
ALU Operations Among Registers

| Operand | Description | Instruction |
|---------|-------------|-------------|
| Rdst    | Register R[0-3], destination | ADD, SUB, AND, OR, MOVE, LSH, RSH |
| Rs1c1   | Source register for ALU operation selection (see Table 2.5-1) |

**Table Content:**
ALU_sel Instruction Operation Description
- **ADD:** Rdst = Rdst + Rdst2 - Add to register
- **SUB:** Rdst = Rdst - Rdst2 - Subtract from register
- **AND:** Rdst = Rdst & Rdst2 - Bitwise logical AND of two operands
- **OR:** Rdst = Rdst | Rdst2 - Bitwise logical OR of two operands
- **MOVE:** Rdst = Rs1c1 - Move to register
- **LSH:** Rdst = Rdst << Rdst2 - Bit shifting left
- **RSH:** Rdst = Rdst >> Rdst2 - Bit shifting right

**Note:**
- ADD or SUB operations can be used to set or clear the overflow flag in ALU.
- All ALU operations can be used to set or clear the zero flag in ALU.

**Footer Information:**
Espressif Systems
311 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback