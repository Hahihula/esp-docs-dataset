

```markdown
| Name                     | Description                                                                 | Address | Access |
|--------------------------|-----------------------------------------------------------------------------|---------|--------|
| mhpmcounter9             | Machine performance-monitoring counter                                     | 0xB09   | R/W    |
| mhpmcounter13            | Machine performance-monitoring counter                                     | 0xBOD   | R/W    |
| mcycleh                  | Upper 32 bits of mcycle                                                    | 0xB80   | R/W    |
| minstreh                 | Upper 32 bits of minstret                                                  | 0xB82   | R/W    |
| mhpmcounter8h            | Upper 32 bits of mhpmcounter8                                               | 0xB88   | R/W    |
| mhpmcounter9h            | Upper 32 bits of mhpmcounter9                                               | 0xB89   | R/W    |
| mhpmcounter13h           | Upper 32 bits of mhpmcounter13                                              | 0xB8D   | R/W    |

Unprivileged/User Mode Counter/Timers
cycle                      | Cycle Counter for RDCYCLE instruction                                      | 0xC00   | RO     |
time                       | Timer for RDTIME instruction                                                | 0xC01   | RO     |
instret                    | Instructions-retired counter for RDINSTRET instruction                      | 0xC02   | RO     |
hpmcounter8                | Performance-monitoring counter                                              | 0xC08   | RO     |
hpmcounter9                | Performance-monitoring counter                                              | 0xC09   | RO     |
hpmcounter13               | Performance-monitoring counter                                              | 0xCOD   | RO     |
cycleh                     | Upper 32 bits of cycle                                                      | 0xC80   | RO     |
instreh                    | Upper 32 bits of instret                                                    | 0xC82   | RO     |
hpmcounter8h               | Upper 32 bits of hpmcounter8                                                | 0xC88   | RO     |
hpmcounter9h               | Upper 32 bits of hpmcounter9                                                | 0xC89   | RO     |
hpmcounter13h              | Upper 32 bits of hpmcounter13                                               | 0xC8D   | RO     |

GPIO Access CSRs (Custom)
cpu_gpio_oen               | GPIO output enable                                                          | 0x803   | R/W    |
cpu_gpio_in                | GPIO input value                                                            | 0x804   | RO     |
cpu_gpio_out               | GPIO output value                                                           | 0x805   | R/W    |

Zc Extension CSRs
jvt                        | Machine table jump base vector and control register                          | 0x017   | R/W    |

Machine Extension Status CSRs (Custom)
mexstatus                  | Machine extension control and status register                                | 0x7E1   | R/W    |
mhint                      | Machine implicit operation register                                          | 0x7C5   | R/W    |

Physical Memory Attributes Checker (PMAC) CSRs (Custom)
pma_cfgn (n: 0-15)          | Physical memory attribute configuration register                             | 0xBC0+0x1*n | R/W |
pma_addrn (n: 0-15)         | Physical memory attribute address register                                   | 0xBD0+0x1*n | R/W |

Bus Error Exception Context CSRs (Custom)
ldpc0                      | Load bus error PC register 0                                                 | 0xBEO   | R/W    |
ldpc1                      | Load bus error PC register 1                                                 | 0xBE1   | R/W    |
ldtval0                    | Load bus error access address register 0                                    | 0xBE8   | R/W    |
ldtval1                    | Load bus error access address register 1                                    | 0xBE9   | R/W    |
stpc0                      | Store bus error PC register 0                                                | 0xBF0   | R/W    |
stpc1                      | Store bus error PC register 1                                                | 0xBF1   | R/W    |
stpc2                      | Store bus error PC register 2                                                | 0xBF2   | R/W    |
sttval0                    | Store bus error access address register 0                                   | 0xBF8   | R/W    |
sttval1                    | Store bus error access address register 1                                   | 0xBF9   | R/W    |
```