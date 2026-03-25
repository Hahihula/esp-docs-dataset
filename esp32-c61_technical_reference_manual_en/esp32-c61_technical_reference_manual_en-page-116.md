

```markdown
## 1.11.2.3 Functional Description

When JAL/JALR/C.JALR instruction is pre-decoded by the core, the 32-bit PC of the next instruction is pushed to RAS.

The address is popped out from RAS when the return type instruction (JALR, C.JR, C.JALR) is pre-decoded by the core. The core then starts fetching from the popped address. On execution of the return instruction, if the popped address does not match the address stored in the link register, then the core flushes the pipeline and starts to fetch from the address in the link register. RAS can store a maximum of four entries of return addresses, that is, four levels of function call nesting are supported.

RAS prediction depends on the following conditions:

| Target Register (Rd) | Source Register (Rs) | RAS action |
|----------------------|----------------------|------------|
| rd != x1             | rs1 != x1            | No action  |
| rd != x1             | rs1 == x1            | POP        |
| rd == x1             | rs1 != x1            | PUSH       |
| rd == x1             | rs1 == x1            | PUSH and POP |

## 1.11.3 Control Status Register for Performance Configuration

Register 1.107. mhcr (0x7C1)

```
| 31           | 13 | 12 | 11 | (reserved) | BTB   | BPE RS | (reserved) |
|--------------|----|----|----|------------|-------|--------|------------|
|              |    |    |    |            |       |        |            |
| 0x00000      | O  | 0x00 | O   | O          | 0x0   | Reset  |

RS Configures whether to enable the return address stack logic for prediction.
O: Disable
1: Enable
(R/W)

BPE Configures whether to enable conditional branch prediction.
O: Disable
1: Enable
(R/W)

BTB Configures whether to enable branch target buffer.
O: Disable
1: Enable
(R/W)
```