

```markdown
| Name                  | Description                                                                 | Address           | Access |
|-----------------------|-----------------------------------------------------------------------------|-------------------|--------|
| pmpaddrn (n: 0-31)    | Physical memory protection address register                                 | 0x3B0+0x1*n       | R/W    |

**Trigger Module CSRs (shared with Debug Mode)**

| tselect               | Trigger select register                                                     | 0x7A0             | R/W    |
| tdata1                | Trigger abstract data 1                                                    | 0x7A1             | R/W    |
| tdata2                | Trigger abstract data 2                                                    | 0x7A2             | R/W    |
| tdata3                | Trigger abstract data 3                                                    | 0x7A3             | R/W    |
| tinfo                 | Trigger information                                                        | 0x7A4             | R/W    |
| tcontrol              | Global trigger control                                                     | 0x7A5             | R/W    |
| mcontext              | Machine mode context register                                              | 0x7A8             | R/W    |

**Debug Mode CSRs (Accessible only in Debug Mode)**

| dcsr                   | Debug control and status                                                   | 0x7B0             | R/W    |
| dpc                    | Debug PC                                                                   | 0x7B1             | R/W    |
| dscratch0              | Debug scratch register 0                                                   | 0x7B2             | R/W    |
| dscratch1              | Debug scratch register 1                                                   | 0x7B3             | R/W    |
| dmcs2                  | Debug mode control status register 2                                       | 0x32              | R/W    |

**Machine Counter Setup**

| mcountinhibit          | Machine counter inhibit register                                            | 0x320             | R/W    |
| mhpmevent8             | Machine performance-monitoring event selector                              | 0x308             | R/W    |
| mhpmevent9             | Machine performance-monitoring event selector                              | 0x329             | R/W    |
| mhpmevent13            | Machine performance-monitoring event selector                              | 0x32D             | R/W    |

**Machine Counter/Timers**

| mcycle                 | Machine cycle counter                                                      | 0xBOO              | R/W    |
| minstret               | Machine instructions-retired counter                                       | 0xB02              | R/W    |
| mhpcounter8            | Machine performance-monitoring counter                                     | 0xB08              | R/W    |
| mhpcounter9            | Machine performance-monitoring counter                                     | 0xB09              | R/W    |
| mhpcounter13           | Machine performance-monitoring counter                                     | 0xBOD              | R/W    |
| mcycleh                | Upper 32 bits of mcycle                                                    | 0xB80              | R/W    |
| minstreh               | Upper 32 bits of minstret                                                  | 0xB82              | R/W    |
| mhpcounter8h           | Upper 32 bits of mhpcounter8                                               | 0xB88              | R/W    |
| mhpcounter9h           | Upper 32 bits of mhpcounter9                                               | 0xB89              | R/W    |
| mhpcounter13h          | Upper 32 bits of mhpcounter13                                              | 0xB8D              | R/W    |

**Unprivileged/User Mode Floating-Point CSRs**

| fflags                 | Floating-point accrued exceptions                                          | 0x001              | R/W    |
| frm                    | Floating-point dynamic rounding mode                                      | 0x002              | R/W    |
| fcscr                  | Floating-point control and status register (frm + fflags)                   | 0x003              | R/W    |

**Unprivileged/User Mode Counter/Timers**

| cycle                  | Cycle Counter for RDCYCLE instruction                                      | 0xC00              | RO     |
| time                   | Timer for RDTIME instruction                                                | 0xC01              | RO     |
| instret                | Instructions-retired counter for RDINSTRET instruction                      | 0xC02              | RO     |
| hpmcounter8            | Performance-monitoring counter                                             | 0xC08              | RO     |
| hpmcounter9            | Performance-monitoring counter                                             | 0xC09              | RO     |
| hpmcounter13           | Performance-monitoring counter                                             | 0xCOD              | RO     |
| cycleh                 | Upper 32 bits of cycle                                                      | 0xC80              | RO     |
```