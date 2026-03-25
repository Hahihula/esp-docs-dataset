
```markdown
| Name               | Description                                                                                   | MCLICBASE Offset | Absolute Address   | Access |
|--------------------|-----------------------------------------------------------------------------------------------|------------------|--------------------|--------|
| clicintctl[7]      | Level control register for CLINT timer interrupts                                             | 0x101F           | 0x2080101F         | R/W    |
| clicintip[16]      | Pending register for external interrupt 0                                                     | 0x1040           | 0x20801040         | R/W    |
| clicintie[16]      | Enable register for external interrupt 0                                                      | 0x1041           | 0x20801041         | R/W    |
| clicintattr[16]    | Attribute register for external interrupt 0                                                   | 0x1042           | 0x20801042         | R/W    |
| clicintctl[16]     | Level control register for external interrupt 0                                              | 0x1043           | 0x20801043         | R/W    |
| clicintip[17]      | Pending register for external interrupt 1                                                     | 0x1044           | 0x20801044         | R/W    |
| clicintie[17]      | Enable register for external interrupt 1                                                      | 0x1045           | 0x20801045         | R/W    |
| clicintattr[17]    | Attribute register for external interrupt 1                                                   | 0x1046           | 0x20801046         | R/W    |
| clicintctl[17]     | Level control register for external interrupt 1                                              | 0x1047           | 0x20801047         | R/W    |
| ...                | ...                                                                                           | ...              | ...                | ...    |
| clicintip[n]       | Pending register for nth external interrupt⁴                                                 | 0x1040 + 4*n     | 0x20801040 + 4*n   | R/W    |
| clicintie[n]       | Enable register for nth external interrupt⁴                                                  | 0x1041 + 4*n     | 0x20801041 + 4*n   | R/W    |
| clicintattr[n]     | Attribute register for nth external interrupt⁴                                               | 0x1042 + 4*n     | 0x20801042 + 4*n   | R/W    |
| clicintctl[n]      | Level control register for nth external interrupt⁴                                          | 0x1043 + 4*n     | 0x20801043 + 4*n   | R/W    |
| ...                | ...                                                                                           | ...              | ...                | ...    |
| clicintip[46]      | Pending register for external interrupt 30                                                   | 0x10B8           | 0x208010B8         | R/W    |
| clicintie[46]      | Enable register for external interrupt 30                                                    | 0x10B9           | 0x208010B9         | R/W    |
| clicintattr[46]    | Attribute register for external interrupt 30                                                  | 0x10BA           | 0x208010BA         | R/W    |
| clicintctl[46]     | Level control register for external interrupt 30                                             | 0x10BB           | 0x208010BB         | R/W    |
| clicintip[47]      | Pending register for external interrupt 31                                                   | 0x10BC           | 0x208010BC         | R/W    |
| clicintie[47]      | Enable register for external interrupt 31                                                    | 0x10BD           | 0x208010BD         | R/W    |
| clicintattr[47]    | Attribute register for external interrupt 31                                                  | 0x10BE           | 0x208010BE         | R/W    |
| clicintctl[47]     | Level control register for external interrupt 31                                             | 0x10BF           | 0x208010BF         | R/W    |
```