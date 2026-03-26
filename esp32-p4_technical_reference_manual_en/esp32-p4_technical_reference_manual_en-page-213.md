

```markdown
Register 3.15. minstreth (0xB82)

MINSTRETH Configures the higher 32 bits of the instruction counter. (R/W)


Register 3.16. mhpmcounter(n: 3-12)h (0xB80+n)

MHPMCOUNTERnh Configures the higher 32 bits of the performance counter n. (R/W)


Register 3.17. mcountinhibit (0x320)

HPM Configures whether the performance counter n(n:3-12) increments.
0: The counter does not count
1: The counter increments
(R/W)

IR Configure whether the instruction counter increments.
0: The counter does not count
1: The counter increments
(R/W)

CY Configure whether the clock cycle counter increments.
0: The counter does not count
1: The counter increments
(R/W)
```