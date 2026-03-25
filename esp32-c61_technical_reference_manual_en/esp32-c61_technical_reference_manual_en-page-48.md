

```markdown
Register 1.14. mtval (0x343)

MTVAL Represents the machine trap value. This is automatically updated with an exception dependent data which may be useful for handling that exception.
Data is to be interpreted depending upon exception IDs:
0x01: Faulting virtual address of instruction
0x02: Faulting instruction opcode
0x05: Faulting data address of load operation
0x07: Faulting data address of store operation
0x1F: Faulting instruction opcode related to illegal PIE instruction
Note: The value of this register is not valid for other exception IDs and interrupts.
(R/W)

Register 1.15. mip (0x344)

All bits are hardwired to 0 since only CLIC mode is available. (RO)
```