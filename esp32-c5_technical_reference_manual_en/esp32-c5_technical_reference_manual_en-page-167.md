

```markdown
Chapter 4 Low-Power CPU

Register 4.10. mip (0x344)

IP Configures the pending status of the interrupt.
O: Not pending
1: Pending
(R/W)

Register 4.11. mcycle (0xB00)

MCYCLE Configures the lower 32 bits of the clock cycle counter. (R/W)

Register 4.12. minstret (0xB02)

MINSTRET Configures the lower 32 bits of the instruction counter. (R/W)

Register 4.13. mhpmcounter(n; 3-12) (0xB00+n)
```