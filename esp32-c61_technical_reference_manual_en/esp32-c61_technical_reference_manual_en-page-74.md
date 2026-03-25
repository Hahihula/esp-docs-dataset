

```markdown
| Instruction | Mnemonic | Description |
|:------------|:----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| c.zext.h    | c.zext.h rsd' | Zero-extends the least significant halfword of the operand to 32 bits by inserting zeros into all of the bits more significant than 15 |
| c.sext.h    | c.sext.h rsd' | Sign-extends the least significant halfword of the operand to 32 bits by copying the most significant bit in the halfword to all the more significant bits |
| c.not       | c.not rsd'   | Takes the one's complement of rd'/rs1' and writes the result to the same register |
| c.mul       | c.mul rsd'   | Multiplies 32 bits of the source operands from rsd' and rs2' and writes the lowest 32 bits to the result to rsd' |

**Zcmp extension**

| cm.push     | cm.push {reg_list}, stack_adj | Stores the registers in reg_list to the memory below the stack pointer, and then creates the stack frame by decrementing the stack pointer by stack_adj, including any additional stack space requested by the value of spinm |
|:------------|:-----------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| cm.pop      | cm.pop {reg_list}, stack_adj | Loads the registers in reg_list from stack memory, and then adjusts the stack pointer by stack_adj |
| cm.popret   | cm.popret {reg_list}, stack_adj | Loads the registers in reg_list from stack memory, adjusts the stack pointer by stack_adj, then return to ra |
| cm.popretz  | cm.popretz {reg_list}, stack_adj | Loads the registers in reg_list from stack memory, adjusts the stack pointer by stack_adj, moves zero to a0 and then return to ra |
| cm.mva01s   | cm.mva01s rs1', rs2'         | Moves r1's into a0 and r2's into a1 |
| cm.mva01    | cm.mva01 r1's, r2's          | Moves a0 into r1's and a1 into r2's |

**Zcmt extension**

| cm.jt       | cm.jt index | Reads an entry from the jump vector table in memory and jumps to the address that was read |
|:------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------|
| cm.jalt     | cm.jalt index | Reads an entry from the jump vector table in memory and jumps to the address that was read, linking to ra |

For more details about the instructions please refer to Zc-specification v1.0.4-3.
```

## 1.6.3.4 Limitations

jvt adds architecture state to the context. Therefore, it must be saved and restored on context switches.