

```markdown
Register 1.10. mcause (0x342)

| 31 | 30 | 5 | 4 | 0 |
|----:|----:|:-:|:-:|:-|
|    |     |   |   | Reset |
| O  |      | 0x0000000 |       |

Exception Code This field is automatically updated with unique ID of the most recent exception or interrupt due to which CPU entered trap. (R/W)
Possible exception IDs are:
* `0x1`: PMP Instruction access fault
* `0x2`: Illegal Instruction
* `0x3`: Hardware Breakpoint/Watchpoint or EBREAK
* `0x5`: PMP Load access fault
* `0x7`: PMP Store access fault
* `0x8`: ECALL from U mode
* `0xb`: ECALL from M mode

Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch.

Interrupt Flag This flag is automatically updated when CPU enters trap. (R/W)
If this is found to be set, indicates that the latest trap occurred due to interrupt. For exceptions it remains unset.
Note: The interrupt controller is using up IDs in range 1-31 for all external interrupt sources. This is different from the RISC-V standard which has reserved IDs in range 0-15 for core internal interrupt sources.

Register 1.11. mtval (0x343)

| 31 | MTVAL | 0 |
|----:|-------|:-|
|    |       | Reset |
| O  | 0x00000000 |       |

MTVAL Machine trap value. (R/W)
This is automatically updated with an exception dependent data which may be useful for handling that exception.
Data is to be interpreted depending upon exception IDs:
* `0x1`: Faulting virtual address of instruction
* `0x2`: Faulting instruction opcode
* `0x5`: Faulting data address of load operation
* `0x7`: Faulting data address of store operation

Note: The value of this register is not valid for other exception IDs and interrupts.
```