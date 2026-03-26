

```markdown
## 1.6.4 Zc (Z) Extension

### 1.6.4.1 Overview

Zc extension is useful for code size reduction. Each HP core implements this extension compatible with **Zc-specification v1.0.4-3**. The Zc-specification has multiple subset extensions, and the ESP32-P4HP CPU has implemented Zcb, Zcmp, and Zcmt extensions.

### 1.6.4.2 Functional Description

#### Zcb Extension

The Zcb extension depends on the C extension and provides more compressed instructions for the following scenarios:

* Immediate and address offset is small.
* Destination register and the first source register are identical.
* The registers used are the 8 most popular ones (x8-x15).

#### Zcmp Extension

The Zcmp extension is a set of instructions which may be executed as a series of existing 32-bit RISC-V instructions.

* PUSH, POP, POPRET operations used to reduce the size of function prologues and epilogues
    * The PUSH operation
        * adjusts the stack pointer to create the stack frame
        * pushes (stores) the registers specified in the register list to the stack frame
    * The POP operation
        * pops (loads) the registers in the register list from the stack frame
        * adjusts the stack pointer to destroy the stack frame
    * The POPRET operation
        * pops (loads) the register in the register list from the stack frame
        * cm.poppretz also moves zero into a0 as the return value
        * adjusts the stack pointer to destroy the stack frame
        * executes a ret instruction to return from the function
    * Move two a0-a1 into two registers of s0-s7
    * Move two s0-s7 into a0-a1

#### Zcmt Extension

The Zcmt extension is also referred to as table jump. It reads the jump target address from the jump table and then jumps to it.
```