

```markdown
Register 4.8. mcause (0x342)

| 31 | 30 | [reserved] | 5 | 4 | 0 |
|----:|----:|-----------:|:-|:-|:-|
|   0 |     | 0x00000000 |   |   | 0x00 |

Exception Code This field is automatically updated with unique ID of the most recent exception or interrupt due to which CPU entered trap. Possible exception IDs are:
- `0x2`: Illegal instruction
- `0x3`: Hardware breakpoint/watchpoint or EBREAK
- `0x6`: Misaligned atomic instructions

Note: Exception ID `0x0` (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch.

(R/W)

Interrupt Flag This flag is automatically updated when CPU enters trap. If this is found to be set, it indicates that the latest trap occurred due to an interrupt. For exceptions it remains unset.

(R/W)

Register 4.9. mtval (0x343)

| 31 | [reserved] | 0 |
|----:|-----------:|:-|
|   0 |     0x00000000 | Reset |

MTVAL Configures machine trap value. This is automatically updated with an exception dependent data which may be useful for handling that exception. Data is to be interpreted depending upon exception IDs:
- `0x1`: Faulting address of instruction
- `0x2`: Faulting instruction opcode
- `0x5`: Faulting data address of load operation
- `0x7`: Faulting data address of store operation

Note: The value of this register is not valid for other exception IDs and interrupts.

(R/W)
```