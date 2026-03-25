

```markdown
| Name                  | Description                                                                                      | MCLICBASE Offset | Absolute Address   | Access |
|-----------------------|--------------------------------------------------------------------------------------------------|------------------|--------------------|--------|
| clicintie[16]         | Enable register for external interrupt 0                                                          | 0x1041           | 0x20801041         | R/W    |
| clicintattr[16]       | Attribute register for external interrupt 0                                                      | 0x1042           | 0x20801042         | R/W    |
| clicinctl[16]         | Level control register for external interrupt 0                                                 | 0x1043           | 0x20801043         | R/W    |
| clicintip[17]         | Pending register for external interrupt 1                                                        | 0x1044           | 0x20801044         | R/W    |
| clicintie[17]         | Enable register for external interrupt 1                                                        | 0x1045           | 0x20801045         | R/W    |
| clicintattr[17]       | Attribute register for external interrupt 1                                                     | 0x1046           | 0x20801046         | R/W    |
| clicinctl[17]         | Level control register for external interrupt 1                                                | 0x1047           | 0x20801047         | R/W    |
| ...                   | ...                                                                                              | ...              | ...                | ...    |
| clicintip[n]          | Pending register for nth external interrupt 6                                                   | 0x1040 + 4*n     | 0x20801040 + 4*n   | R/W    |
| clicintie[n]          | Enable register for nth external interrupt 6                                                    | 0x1041 + 4*n     | 0x20801041 + 4*n   | R/W    |
| clicintattr[n]        | Attribute register for nth external interrupt 6                                                 | 0x1042 + 4*n     | 0x20801042 + 4*n   | R/W    |
| clicinctl[n]          | Level control register for nth external interrupt 6                                             | 0x1043 + 4*n     | 0x20801043 + 4*n   | R/W    |
| ...                   | ...                                                                                              | ...              | ...                | ...    |
| clicintip[46]         | Pending register for external interrupt 30                                                      | 0x10B8           | 0x208010B8         | R/W    |
| clicintie[46]         | Enable register for external interrupt 30                                                       | 0x10B9           | 0x208010B9         | R/W    |
| clicintattr[46]       | Attribute register for external interrupt 30                                                    | 0x10BA           | 0x208010BA         | R/W    |
| clicinctl[46]         | Level control register for external interrupt 30                                                | 0x10BB           | 0x208010BB         | R/W    |
| clicintip[47]         | Pending register for external interrupt 31                                                      | 0x10BC           | 0x208010BC         | R/W    |
| clicintie[47]         | Enable register for external interrupt 31                                                       | 0x10BD           | 0x208010BD         | R/W    |
| clicintattr[47]       | Attribute register for external interrupt 31                                                    | 0x10BE           | 0x208010BE         | R/W    |
| clicinctl[47]         | Level control register for external interrupt 31                                                | 0x10BF           | 0x208010BF         | R/W    |

### 1.8.2.7 CLIC Memory-Mapped Register Description

Register 1.72. mcliccfg (0x20800000)

```
| 31                    | 6   5   4   3   2   1   0 |
|-----------------------|-----------------------------|
|                       | NMBITS OxO                  |
|                       | MNLBITS OxO                 |
|                       | Reset                      |

MNLBITS Configures the number of upper bits that are used globally (for HP core) to encode the interrupt level in all the 8-bit clicinctl[i] registers for each machine mode interrupt. The only allowed values are in the range 0-8. Any higher value will be clamped to 8. (R/W)

NMBITS Configures the number of bits in clicintattr[j].MODE to be used globally (for HP core) to represent the mode of an interrupt. For systems with machine mode only, this is hardwired to 0. This indicates that the clicintattr[j].MODE field is hardwired to 0x3 and therefore all interrupts are in machine mode only. (RO)
```