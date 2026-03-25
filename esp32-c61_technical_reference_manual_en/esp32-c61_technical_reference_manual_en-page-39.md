

```markdown
| Name               | Description                                                                                      | Address   | Access |
|--------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| ustatus            | User mode status                                                                                 | 0x000     | R/W    |
| utvec<sup>4</sup>   | User trap vector                                                                                | 0x005     | R/W    |
| utvt               | User vector interrupt base address (Refer to CLIC specifications)                               | 0x007     | R/W    |
|                    |                                              |           |        |
| **User Trap Handling CSRs** |                                                  |           |        |
| uscratch           | User scratch                                                                                    | 0x040     | R/W    |
| uepc               | User trap program counter                                                                       | 0x041     | R/W    |
| ucause<sup>5</sup>  | User trap cause                                                                                 | 0x042     | R/W    |
| unxti              | Interrupt handler address and enable modifier (Refer to CLIC specifications)                    | 0x045     | R/W    |
| uintthresh         | Interrupt threshold (Refer to CLIC specifications)                                              | 0x047     | R/W    |
| uclibase           | User mode interrupt controller base address register (CUSTOM) (Refer to CLIC specifications)   | 0x050     | RO     |
| uintstatus         | Current interrupt levels (Refer to CLIC specifications)                                         | 0xCB1     | RO     |
|                    |                                              |           |        |
| **Physical Memory Protection (PMP) CSRs** |                                                  |           |        |
| pmcfg0             | Physical memory protection configuration                                                      | 0x3A0     | R/W    |
| pmcfg1             | Physical memory protection configuration                                                      | 0x3A1     | R/W    |
| pmcfg2             | Physical memory protection configuration                                                      | 0x3A2     | R/W    |
| pmcfg3             | Physical memory protection configuration                                                      | 0x3A3     | R/W    |
| pmpaddrn (n: 0-15) | Physical memory protection address register                                                    | 0x3B0+0x1*n| R/W    |
|                    |                                              |           |        |
| **Trigger Module CSRs (shared with Debug Mode)** |                                                  |           |        |
| tselect            | Trigger select register                                                                        | 0x7A0     | R/W    |
| tdata1             | Trigger abstract data 1                                                                        | 0x7A1     | R/W    |
| tdata2             | Trigger abstract data 2                                                                        | 0x7A2     | R/W    |
| tdata3             | Trigger abstract data 3                                                                        | 0x7A3     | R/W    |
| tinfo              | Trigger information                                                                            | 0x7A4     | R/W    |
| tcontrol           | Global trigger control                                                                         | 0x7A5     | R/W    |
| mcontext           | Machine mode context register                                                                  | 0x7A8     | R/W    |
|                    |                                              |           |        |
| **Debug Mode CSRs (Accessible only in Debug Mode)** |                                                  |           |        |
| dcsr               | Debug control and status                                                                       | 0x7B0     | R/W    |
| dpc                | Debug PC                                                                                       | 0x7B1     | R/W    |
| dscratch0          | Debug scratch register 0                                                                       | 0x7B2     | R/W    |
| dscratch1          | Debug scratch register 1                                                                       | 0x7B3     | R/W    |
|                    |                                              |           |        |
| **Machine Counter Setup** |                                                  |           |        |
| mcountinhibit      | Machine counter inhibit register                                                               | 0x320     | R/W    |
| mhpvente8          | Machine performance-monitoring event selector                                                 | 0x308     | R/W    |
| mhpvente9          | Machine performance-monitoring event selector                                                 | 0x329     | R/W    |
| mhpvente13         | Machine performance-monitoring event selector                                                 | 0x32D     | R/W    |
|                    |                                              |           |        |
| **Machine Counter/Timers** |                                                  |           |        |
| mcycle             | Machine cycle counter                                                                          | 0xB00     | R/W    |
| minstret           | Machine instructions-retired counter                                                          | 0xB02     | R/W    |
| mhpcounter8        | Machine performance-monitoring counter                                                        | 0xB08     | R/W    |
```