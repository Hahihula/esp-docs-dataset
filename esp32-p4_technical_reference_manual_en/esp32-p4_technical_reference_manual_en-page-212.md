

```markdown
Chapter 3 Low-Power CPU
GoBack

Register 3.11. mcycle (0xB00)

mcycle

31 | mcycle | 0
0x0 | Reset

MCYCLE Configures the lower 32 bits of the clock cycle counter. (R/W)

Register 3.12. minstret (0xBO2)

minstret

31 | minstret | 0
0x0 | Reset

MINSTRET Configures the lower 32 bits of the instruction counter. (R/W)

Register 3.13. mhpcounter(n: 3-12) (0xB00+n)

mhpcounter n

31 | mhpcounter n | 0
0x0 | Reset

MHPMCOUNTERn Configures the lower 32 bits of the performance counter n. (R/W)

Register 3.14. mcycleh (0xB80)

mcycleh

31 | mcycleh | 0
0x0 | Reset

MCYCLEH Configures the higher 32 bits of the clock cycle counter. (R/W)
```