
```markdown
## 2.6.3 Code Size Reduction (Zc) Extension

### 2.6.3.1 Overview

Zc extension is useful for code size reduction. HP core implements this extension compatible with Zc-specification v1.0.4-3. The Zc-specification has multiple subset extensions, and the ESP32-C5HP CPU core has implemented the Zcmt extension.

### 2.6.3.2 Functional Description

**Zcmt Extension**

The Zcmt extension is also referred to as table jump. It reads the jump target address from the jump table and then jumps to it.

Table jump uses a 256-entry 32-bit wide table in instruction memory to contain the function address. The table must be a minimum of 64-byte aligned. It is used as a form of dictionary compression to reduce the code size of jal, auipc+jalr, jr, auipc+jr instructions.

Table jump allows the linker to replace the following instruction sequences with a cm.jalt encoding, and an entry in the table:

*   32-bit j calls
*   32-bit jal ra calls

### 2.6.3.3 Zc Instructions

| Instruction | Mnemonic | Description |
|-------------|-----------|-------------|
| **Zcmt extension** | | |
| cm.jt | cm.jt index | Reads an entry from the jump vector table in memory and jumps to the address that was read |
| cm.jalt | cm.jalt index | Reads an entry from the jump vector table in memory and jumps to the address that was read, linking to ra |

For more details about the instructions please refer to Zc-specification v1.0.4-3.

### 2.6.3.4 Limitations

jvt adds architecture state to the context. Therefore, it must be saved and restored on context switches.
```