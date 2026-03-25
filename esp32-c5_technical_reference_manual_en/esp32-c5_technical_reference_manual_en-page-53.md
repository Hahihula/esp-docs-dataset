

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| Trigger Module CSRs (shared with Debug Mode) |                                                                             |         |        |
| tselect                                    | Trigger select register                                                     | 0x7A0   | R/W    |
| tdata1                                     | Trigger abstract data 1                                                     | 0x7A1   | R/W    |
| tdata2                                     | Trigger abstract data 2                                                     | 0x7A2   | R/W    |
| tdata3                                     | Trigger abstract data 3                                                     | 0x7A3   | R/W    |
| tinfo                                      | Trigger information                                                         | 0x7A4   | R/W    |
| tcontrol                                   | Global trigger control                                                      | 0x7A5   | R/W    |
| mcontext                                   | Machine mode context register                                               | 0x7A8   | R/W    |
| Debug Mode CSRs (Accessible only in Debug Mode) |                                                                             |         |        |
| dcsr                                       | Debug control and status                                                   | 0x7B0   | R/W    |
| dpc                                        | Debug PC                                                                   | 0x7B1   | R/W    |
| dscratch0                                  | Debug scratch register 0                                                   | 0x7B2   | R/W    |
| dscratch1                                  | Debug scratch register 1                                                   | 0x7B3   | R/W    |
| Machine Counter Setup                      |                                                                             |         |        |
| mcountinhibit                              | Machine counter inhibit register                                            | 0x320   | R/W    |
| mhpmevent8                                 | Machine performance-monitoring event selector                               | 0x308   | R/W    |
| mhpmevent9                                 | Machine performance-monitoring event selector                               | 0x329   | R/W    |
| mhpmevent13                                | Machine performance-monitoring event selector                               | 0x32D   | R/W    |
| Machine Counter/Timers                     |                                                                             |         |        |
| mcycle                                     | Machine cycle counter                                                       | 0xB00   | R/W    |
| minstret                                   | Machine instructions-retired counter                                       | 0xB02   | R/W    |
| mhpcounter8                                | Machine performance-monitoring counter                                     | 0xB08   | R/W    |
| mhpcounter9                                | Machine performance-monitoring counter                                     | 0xB09   | R/W    |
| mhpcounter13                               | Machine performance-monitoring counter                                     | 0xB0D   | R/W    |
| mcycleh                                    | Upper 32 bits of mcycle                                                     | 0xB80   | R/W    |
| minstreh                                   | Upper 32 bits of minstret                                                   | 0xB82   | R/W    |
| mhpcounter8h                               | Upper 32 bits of mhpcounter8                                                | 0xB88   | R/W    |
| mhpcounter9h                               | Upper 32 bits of mhpcounter9                                                | 0xB89   | R/W    |
| mhpcounter13h                              | Upper 32 bits of mhpcounter13                                               | 0xB8D   | R/W    |
| Unprivileged/User Mode Counter/Timers      |                                                                             |         |        |
| cycle                                      | Cycle Counter for RDCYCLE instruction                                       | 0xC00   | RO     |
| time                                       | Timer for RDTIME instruction                                                 | 0xC01   | RO     |
| instret                                    | Instructions-retired counter for RDINSTRET instruction                       | 0xC02   | RO     |
| hpmcounter8                                 | Performance-monitoring counter                                              | 0xC08   | RO     |
| hpmcounter9                                 | Performance-monitoring counter                                              | 0xC09   | RO     |
| hpmcounter13                                | Performance-monitoring counter                                              | 0xC0D   | RO     |
| cycleh                                     | Upper 32 bits of cycle                                                      | 0xC80   | RO     |
| instreth                                   | Upper 32 bits of instret                                                    | 0xC82   | RO     |
| hpmcounter8h                               | Upper 32 bits of hpmcounter8                                                | 0xC88   | RO     |
| hpmcounter9h                               | Upper 32 bits of hpmcounter9                                                | 0xC89   | RO     |
| hpmcounter13h                              | Upper 32 bits of hpmcounter13                                               | 0xC8D   | RO     |
| Custom System CSRs (Custom)                |                                                                             |         |        |
| GPIO Access CSRs (Custom)                  |                                                                             |         |        |
```