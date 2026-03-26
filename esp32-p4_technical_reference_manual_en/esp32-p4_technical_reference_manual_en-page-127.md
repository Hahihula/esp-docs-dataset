

```markdown
## 1.9.2.7 CLIC Memory-Mapped Register Description

### Register 1.94. mcliccfg (0x20800000)

| Bit | Field Name   | Reset Value |
|-----|--------------|-------------|
| 30  |             | 0x0000      |
|     |              |             |
|     | NMBITS       | 0x0         |
|     | MNLBITS      | 1           |

**MNLBITS**: Configures the number of upper bits that are used globally (for each HP core) to encode the interrupt level in all the 8-bit `clicintctl[i]` registers for each machine mode interrupt. The only allowed values are in the range 0-8. Any higher value will be clamped to 8. (R/W)

**NMBITS**: Configures the number of bits in `clicintattr[j].MODE` to be used globally (for each HP core) to represent the mode of an interrupt. For systems with machine mode only, this is hardwired to 0. This indicates that the `clicintattr[j].MODE` field is hardwired to 0x3 and therefore all interrupts are in machine mode only. (RO)

### Register 1.95. clicinfo (0x20800004)

| Bit | Field Name           | Reset Value |
|-----|----------------------|-------------|
| 31  |                      |             |
|     | NUM_INTERRUPTS       | 0x0030      |
|     | CLICINTCTLBITS       | 0x03        |

**NUM_INTERRUPTS**: Represents the number of interrupts supported by this implementation of CLIC. Hardwired to 48. (RO)

**CLICINTCTLBITS**: Represents the number of higher bits which are actually programmable in the 8-bit `clicintctl[i]` registers. Hardwired to 0x3. (RO)
```