

```markdown
Register 2.84. dcsr (0x7B0)

Continued from the previous page...

step When set and not in debug mode, the core will only execute a single instruction and then enter debug mode.
If the instruction does not complete due to an exception, the core will immediately enter debug mode before executing the trap handler, with appropriate exception registers set.
Setting this bit does not mask interrupts. This is a deviation from the RISC-V External Debug Support Specification Version 0.13.
(R/W)

prv Contains the privilege level the core was operating in when debug mode was entered. A debugger can change this value to change the core's privilege level when exiting debug mode.
Only 0x3 (machine mode) and 0x0 (user mode) are supported. (R/W)


Register 2.85. dpc (0x7B1)

dpc

| 31 | 0 | Reset |
|----|---|-------|

dpc Upon entry to debug mode, dpc is written with the virtual address of the next instruction to be executed. When resuming, the CPU core's PC is updated to the virtual address stored in dpc. A debugger may write dpc to change where the CPU resumes. (R/W)

Table 2.10-3. Virtual address in DPC upon Debug Mode Entry

| Cause           | Virtual Address in DPC                                                                 |
|-----------------|-----------------------------------------------------------------------------------------|
| ebreak          | Address of ebreak instruction                                                           |
| Single Step     | Address of the instruction that would be executed next if no debugging was going on i.e. pc+4 for 32-bit instruction that don't change program flow, the destination PC on taken jumps/branches, etc. |
| Trigger Module  | If timing is 0, the address of the instruction which caused the trigger to fire.<br>If timing is 1, the address of next instruction to be executed at the time that debug mode was entered. |
| Halt Request    | Address of the next instruction to be executed at the time that debug mode was entered.   |

Espressif Systems
```