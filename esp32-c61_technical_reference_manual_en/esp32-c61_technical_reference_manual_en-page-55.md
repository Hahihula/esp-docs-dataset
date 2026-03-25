

```markdown
Register 1.27. ucause (0x042)

| 31 | 30 | 29 | 28 | 27 | 26 | 24 | 23 | 16 | 15 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|
|   0 |   0 | 0x00|    1| 0x0|     |      |      | 0x00| 0x000|    |    | Reset |

INT Represents whether the CPU entered a trap due to interrupts.
O: The trap occurred due to an exception.
1: The trap occurred due to an interrupt.
(R/W)

UINHV Represents whether uepc is an address of an instruction or an address of a vector table entry.
1: Address of a table entry
O: Address of an instruction
(R/W)

UPIE Represents the previous interrupt enable, same as ustatus.UPIE. (R/W)

UPIL Represents the previous 8-bit interrupt level. (R/W)

CODE Represents the unique ID of the most recent exception or interrupt due which CPU entered trap. Possible exception IDs are:
0x01: Instruction access fault
0x02: Illegal instruction
0x03: Hardware breakpoint/watchpoint or EBREAK
0x05: PMP load access fault
0x06: Misaligned store address or AMO address
0x07: Store access or AMO access fault
0x08: ECALL from U mode
0x0b: ECALL from M mode
0x1f: Illegal PIE instruction
Other exception IDs are reserved.
Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch.
(R/W)
```