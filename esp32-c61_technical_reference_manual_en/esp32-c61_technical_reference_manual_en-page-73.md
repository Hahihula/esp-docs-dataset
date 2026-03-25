
```markdown
## 1.6.3 Code Size Reduction (Zc) Extension

### 1.6.3.1 Overview

Zc extension is useful for code size reduction. HP core implements this extension compatible with Zc-specification v1.0.4-3. The Zc-specification has multiple subset extensions, and the ESP32-C61HP CPU has implemented Zcb, Zcmp, and Zcmt extensions.

### 1.6.3.2 Functional Description

#### Zcmt Extension

The Zcmt extension is also referred to as table jump. It reads the jump target address from the jump table and then jumps to it.

Table jump uses a 256-entry 32-bit wide table in instruction memory to contain function address. The table must be a minimum of 64-byte aligned. It is used as a form of dictionary compression to reduce the code size of jal, auipc+jalr, jr, auipc+jr instructions.

Table jump allows the linker to replace the following instruction sequences with a cm.jalt encoding, and an entry in the table:

*   32-bit j calls
*   32-bit jal ra calls

### 1.6.3.3 Zc Instructions

| Instruction | Mnemonic | Description |
|-------------|-----------|-------------|
| **Zcb extension** | | |
| c.lbu | c.lbu rd', uimm(rs1') | Loads a byte from the memory address formed by adding rs1' to the zero-extended immediate uimm. The resulting byte is zero-extended to 32 bits and is written to rd' |
| c.lhu | c.lhu rd', uimm(rs1') | Loads a halfword from the memory address formed by adding rs1' to the zero-extended immediate uimm. The resulting byte is zero-extended to 32 bits and is written to rd' |
| c.lh | c.lh rd', uimm(rs1') | Loads a halfword from the memory address formed by adding rs1' to the zero-extended immediate uimm. The resulting byte is sign-extended to 32 bits and is written to rd' |
| c.sb | c.sb rs2', uimm(rs1') | Stores the least significant byte of rs2' to the memory address formed by adding rs1' to the zero-extended immediate uimm |
| c.sh | c.sh rs2', uimm(rs1') | Stores the least significant halfword of rs2' to the memory address formed by adding rs1' to the zero-extended immediate uimm |
| c.zext.b | c.zext.b rsd' | Zero-extends the least significant byte of the operand to 32 bits by inserting zeros into all of the bits more significant than 7 |
| c.sext.b | c.sext.b rsd' | Sign-extends the least significant byte of the operand to 32 bits by copying the most significant bit in the byte to all the more significant bits |
```