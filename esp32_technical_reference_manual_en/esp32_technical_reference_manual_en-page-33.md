**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
ALU_sel Instruction Operation Description

**Table Content:**
- **Column Headers:** ALU_sel, Instruction, Operation, Description
- **Rows:**
  - Row for "0", "ADD", "Rdst = Rs1 + Imm", "Add to register"
  - Row for "1", "SUB", "Rdst = Rs1 - Imm", "Subtract from register"
  - Row for "2", "AND", "Rdst = Rs1 & Imm", "Bitwise logical AND of two operands"
  - Row for "3", "OR", "Rdst = Rs1 | Imm", "Bitwise logical OR of two operands"
  - Row for "4", "MOVE", "Rdst = Rsrc", "Move to register"
  - Row for "5", "LSH", "Rdst = Rs1 << Imm", "Bit shifting left"
  - Row for "6", "RSH", "Rdst = Rs1 >> Imm", "Bit shifting right"

**Subsection Title:**
Table 1.4-2. ALU Operations with Immediate Value

**Note Section:**
- ADD/SUB operations can be used to set/clear the overflow flag in ALU.
- All ALU operations can be used to set/clear the zero flag in ALU.

**Subsection Header:**
1.4.1.3 Operations with Stage Count Register

**Figure Caption and Description:**
- **Figure 1.4-4:** Instruction Type — ALU for Operations with Stage Count Register
- Text explains that ALU can increment/decrement by a given value, or reset the 8-bit register Stage_cnt to specific values (e.g., bits [27:25] should be set to '3'b2'). The operation depends on instruction's bits presented in Table 1.4-3.

**Table Content for Subsection Header:**
- **Column Headers:** Operand, Description
- **Rows:**
  - Row with "ALU_sel", "Type of ALU operation"
  - Row with "Stage_cnt", "Stage count register, a separate register [7:0] used to store variables such as loop index Imm."
  - Row with "8-bit value"

**Table for Subsection Header (Continued):**
- **Column Headers:** ALU_sel, Instruction Operation
- **Rows:**
  - Row with "0", "STAGE_INC", "Stage_cnt = Stage_cnt + Imm"
  - Row with "1", "STAGE_DEC", "Stage_cnt = Stage_cnt - Imm"
  - Row with "2", "STAGE_RST", "Reset stage count register"

**Subsection Header:**
Table 1.4-3. ALU Operations with Stage Count Register

**Figure Caption and Description for Subsection Header (Continued):**
- **Figure 1.4-5:** Instruction Type — ST
- Text explains that the instruction type is "ST" which stands for Store Data in Memory.

**Footer:**
Espressif Systems, Submit Documentation Feedback ESP32 TRM (Version 5.6) Page number at bottom center - 33