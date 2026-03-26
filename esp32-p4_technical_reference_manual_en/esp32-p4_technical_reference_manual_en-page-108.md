

```markdown
| Instruction | Mnemonic                     | Description                                                                                                                                              |
|-------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| cm.pop      | cm.pop stack_adj             | {reg_list}. Loads the registers in reg_list from stack memory, and then adjusts the stack pointer by stack_adj |
| cm.poppret  | cm.poppret stack_adj         | {reg_list}. Loads the registers in reg_list from stack memory, adjusts the stack pointer by stack_adj, then return to ra |
| cm.poppretz | cm.poppretz stack_adj        | {reg_list}. Loads the registers in reg_list from stack memory, adjusts the stack pointer by stack_adj, moves zero to a0 and then return to ra |
| cm.mva01s   | cm.mva01s rs1', rs2'         | Moves r1's into a0 and r2's into a1                                                                                                                     |
| cm.mva01    | cm.mva01 r1's, r2's          | Moves a0 into r1's and a1 into r2's                                                                                                                    |

Zcmt extension
| cm.jt       | cm.jt index                  | Reads an entry from the jump vector table in memory and jumps to the address that was read |
| cm.jalt     | cm.jalt index                | Reads an entry from the jump vector table in memory and jumps to the address that was read, linking to ra |

For more details about the instructions please refer to Zc-specification v1.0.4-3.

1.6.4.4 Limitations
jvt adds architecture state to the context. Therefore, it must be saved and restored on context switches.
```