

```markdown
Register 2.13. mcause (0x342)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 24 | 23 | 16 | 15 | 6 | 5 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|---|---|---|
|     | INT | MINHV | MPP | MPIL | (reserved) | MPL | (reserved) | CODE | Reset |

INT Represents whether the CPU entered a trap due to interrupts.
O: The trap occurred due to an exception.
1: The trap occurred due to an interrupt.
(R/W)

MINHV Represents whether mepc is an address of an instruction or an address of a vector table entry.
1: Address of a table entry
0: Address of an instruction
(R/W)

MPP Represents the previous privilege mode, same as mstatus.MPP. (R/W)

MPIE Represents the previous interrupt enable, same as mstatus.MPIE. (R/W)

MPIL Represents the previous 8-bit interrupt level. (R/W)

CODE Represents the unique ID of the most recent exception or interrupt due to which CPU entered trap. Possible exception IDs are:
Ox01: Instruction access fault
Ox02: Illegal instruction
Ox03: Hardware breakpoint/watchpoint or EBREAK
Ox05: PMP load access fault
Ox06: Misaligned store address or AMO address
Ox07: Store access or AMO access fault
Ox08: ECALL from U mode
Ox0b: ECALL from M mode
Ox1f: Illegal PIE instruction
Other exception IDs are reserved.
Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch.
(R/W)
```