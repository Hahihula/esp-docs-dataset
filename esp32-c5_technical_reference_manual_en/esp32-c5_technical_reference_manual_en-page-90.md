

```markdown
Register 2.66. clicintattr[i] (0x20801002 + 4*i)

| MODE | (reserved) | TRIG | SHV |
|:-----|:-----------|:------|:-----|
| 7    | 6          | 5     | 3    | 2    | 1    | 0    |
| 0x3  | 0x0        | 0x0   | 0x0  |      |      | Reset |

SHV Configures hardware vectoring for the ith CLIC machine mode interrupt.
0: ith interrupt is not hardware vectored. It means that upon taking this interrupt, the CPU will jump to the address configured in mtvec.
1: ith interrupt is hardware vectored. It means that upon taking this interrupt, the CPU will jump to the word address stored at (mtvt + 4*i) relative to the base address configured in mtvt.
(R/W)

TRIG Configures the trigger type and polarity of the ith CLIC machine mode interrupt.
0x0: interrupt is positive level-triggered
0x1: interrupt is positive edge-triggered
0x2: interrupt is negative level-triggered
0x3: interrupt is negative edge-triggered
(R/W)

MODE Configures the privilege mode of the ith CLIC interrupt.
This is hardwired to 0x3 as user mode interrupts are not supported.
(RO)

Register 2.67. clicintctl[i] (0x20801003 + 4*i)

| CTL[i] | (reserved) |
|--------|------------|
| 7      | 5          | 4    | 0    |
| 0x0    |            | 0x1f | Reset |

CTL[i] Configures the level and priority of the ith CLIC machine mode interrupt.
* Since the CLICINTCTLBITS parameter is 3 in this implementation of CLIC, therefore the actual number of bits implemented in clicintctl[i] is the same, and thus the lower 5 bits of this register are hardwired to 1.
* The configured value of mcliccfg.MNLBITS determines the number of higher bits in clicintctl[i] which encode the level of the interrupt, while the remaining lower bits encode the priority.
(R/W)
```