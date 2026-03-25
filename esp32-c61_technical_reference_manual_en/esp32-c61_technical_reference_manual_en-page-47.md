

```markdown
Register 1.13. mcause (0x342)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  | INT     | Represents whether the CPU entered a trap due to interrupts.<br>0: The trap occurred due to an exception.<br>1: The trap occurred due to an interrupt. (R/W) |
| 30  | MINHV   | Represents whether `mepc` is an address of an instruction or an address of a vector table entry.<br>1: Address of a table entry<br>0: Address of an instruction (R/W) |
| 29  | MPP     | Represents the previous privilege mode, same as `mstatus.MPP`. (R/W)         |
| 28  | MPIE    | Represents the previous interrupt enable, same as `mstatus.MPIE`. (R/W)      |
| 27  | MPIL    | Represents the previous 8-bit interrupt level. (R/W)                         |
| 24-6 | (reserved) |                                                                             |
| 5   | CODE    | Represents the unique ID of the most recent exception or interrupt due to which CPU entered trap.<br>Possible exception IDs are:<br>0x01: Instruction access fault<br>0x02: Illegal instruction<br>0x03: Hardware breakpoint/watchpoint or EBREAK<br>0x05: PMP load access fault<br>0x06: Misaligned store address or AMO address<br>0x07: Store access or AMO access fault<br>0x08: ECALL from U mode<br>0x0b: ECALL from M mode<br>0x1f: Illegal PIE instruction<br>Other exception IDs are reserved.<br>Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch. (R/W) |
| 4   |         |                                                                             |
| 3   |         |                                                                             |
| 2   |         |                                                                             |
| 1   | OxD     |                                                                             |
| 0   | 0x00    |                                                                             |

Reset
```