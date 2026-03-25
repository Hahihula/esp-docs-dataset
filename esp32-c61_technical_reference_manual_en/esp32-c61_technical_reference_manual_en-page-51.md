

```markdown
Register 1.20. mscratchcswl (0x349)

MSCRATCHCSWL Configures the MSCRATCH value by conditionally swapping its value with RS1, based on the current interrupt level in mintstatus.MIL and the previous interrupt level in mcause.MPIL.

This is the conditional scratch swap CSR, which allows performing a scratch value swap conditionally, based on interrupt level change, in a single instruction.

When using CSRRW instruction to access this CSR, the value written into RD is either that of MSCRATCH, if only one of mcause.MPIL and mintstatus.MIL is equal to zero, or RS1 for all other cases.

The value of MSCRATCH is updated with the initial value of RS1 only if one of mcause.MPIL and mintstatus.MIL is equal to zero.
(R/W)

Register 1.21. mclicbase (0x350)

MCICBASE Represents the base address of the CLIC memory-mapped registers for machine mode. (RO)
```