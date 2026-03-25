

```markdown
|31|Ox0|3|2|1|0|
|---|----|---|---|---|---|
|||0x0|0x0|0x0|Reset|

CY Configure whether the clock cycle counter increments.
0: The counter does not count
1: The counter increments
(R/W)

IR Configure whether the instruction counter increments.
0: The counter does not count
1: The counter increments
(R/W)

HPM Configures whether the performance counter n(n:3-12) increments.
0: The counter does not count
1: The counter increments
(R/W)
```

## 4.3 Interrupts and Exceptions

The LP CPU handles interrupts and exceptions according to RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. After entering an interrupt/exception handler, the CPU:

- Saves the current program counter (PC) value to the `mepc` CSR
- Copies the state of MIE of mstatus to MPIE of mstatus
- Saves the current privileged mode to MPP of mstatus
- Clears MIE of mstatus
- Toggles the privileged mode to machine mode (M mode)
- Jumps to the handler address

  - For exceptions, the handler address is the base address of the vector table in the `mtvec` CSR.
  - For interrupts, the handler address is `mtvec + 4 * 30`.

- After the mret instruction is executed, the core jumps to the PC saved in the `mepc` CSR and restores the value of MPIE of mstatus to MIE of mstatus and the privileged mode to that configured by MPP.

When the core starts up, the base address of the vector table is initialized to the boot address 0x50000000. After startup, the base address can be changed by writing to the `mtvec` CSR. For more information about CSRs, see Section 4.2.1.

The core fetches instructions from address 0x50000080 after reset.
```