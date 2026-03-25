

```markdown
Register 1.73. clicinfo (0x20800004)

| 31 | 25 | 24 | 21 | 20 | (reserved) | 13 | 12 | NUM_INTERRUPTS |
|----:|----:|----:|----:|----:|------------:|----:|----:|---------------|
| 0x00 |    | 0x3 |    |    |            |    |    | 0x0030         |

NUM_INTERRUPTS Represents the number of interrupts supported by this implementation of CLIC.
Hardwired to 48. (RO)

CLICINTCTLBITS Represents the number of higher bits which are actually programmable in the 8-bit clicintctl[i] registers. Hardwired to 0x3. (RO)


Register 1.74. clicintip[i] (0x20801000 + 4*i)

IP[i] Represents the pending state for ith CLIC machine mode interrupt.
0: ith interrupt is not pending
1: ith interrupt is pending

- When the ith interrupt is configured as level type using clicintattr[i].TRIG, this bit is read-only,
  and to clear it the interrupt must be cleared from source.
- When the ith interrupt is configured as edge triggered using clicintattr[i].TRIG, this bit is R/W,
  and thus it is to be cleared by writing 0 to this register.

(R/W)


Register 1.75. clicintie[i] (0x20801001 + 4*i)

IE[i] Configures whether to enable the ith CLIC machine mode interrupt.
0: Disable
1: Enabled

(R/W)
```