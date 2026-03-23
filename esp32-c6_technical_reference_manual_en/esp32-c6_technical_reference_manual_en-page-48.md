

```markdown
Register 1.12. mcause (0x342)

| 31 | 30 | [reserved] | 5 | 4 | 0 |
|----:|----:|-----------:|:-|:-|:-|
|   0 |     | 0x00000000 |   |    | 0x00 Reset |

**Exception Code** This field is automatically updated with unique ID of the most recent exception or interrupt due to which CPU entered trap. Possible exception IDs are:

- `0x1`: PMP instruction access fault
- `0x2`: Illegal instruction
- `0x3`: Hardware breakpoint/watchpoint or EBREAK
- `0x5`: PMP load access fault
- `0x6`: Misaligned store address or AMO address
- `0x7`: PMP store access or AMO access fault
- `0x8`: ECALL from U mode
- `0xb`: ECALL from M mode

Other values: reserved

Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch.

(R/W)

**Interrupt Flag** This flag is automatically updated when CPU enters trap.

If this is found to be set, indicates that the latest trap occurred due to an interrupt. For exceptions it remains unset.

Note: The interrupt controller is using up IDs in range 1-2, 5-6 and 8-31 for all external interrupt sources. This is different from the RISC-V standard which has reserved IDs in range 0-15 for core local interrupts only. Although local interrupt sources (CLINT) do use the reserved IDs 0, 3, 4 and 7.

(R/W)
```