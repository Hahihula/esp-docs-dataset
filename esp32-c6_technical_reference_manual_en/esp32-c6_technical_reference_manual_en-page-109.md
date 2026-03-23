

```markdown
| Name                  | Description                                                                 | Address   | Access |
|-----------------------|-----------------------------------------------------------------------------|-----------|--------|
| mcycle                | Machine Clock Cycle Counter                                                 | 0xB00     | R/W    |
| minstret              | Machine Retired Instruction Counter                                        | 0xB02     | R/W    |
| mhpccountern(n:3-12)  | Machine Performance Monitor Counter                                         | 0xB00+n   | R/W    |
| mcycleh               | The higher 32 bits of mcycle                                                | 0xB80     | R/W    |
| minstreh              | The higher 32 bits of minstret                                              | 0xB82     | R/W    |
| mhpcounternh(n:3-12)  | The higher 32 bits of mhpccountern(n:3-12)                                  | 0xB80+n   | R/W    |

Machine Counter Setup CSR

mcounthibit           | Machine Counter Control                                                     | 0x320     | R/W    |
```

Note that if write, set, or clear operation is attempted on any of the read-only (RO) CSRs indicated in the above table, the CPU will generate an illegal instruction exception.

### 3.2.2 Registers

Register 3.1. mhartid (0xF14)

```markdown
MHARTID Represents Hart ID. The LP CPU hart ID is 1. (RO)
```
```