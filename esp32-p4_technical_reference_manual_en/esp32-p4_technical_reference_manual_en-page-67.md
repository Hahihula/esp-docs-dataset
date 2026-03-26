

```markdown
| Name                  | Description                                                                 | Address   | Access |
|-----------------------|-----------------------------------------------------------------------------|-----------|--------|
| instreth              | Upper 32 bits of `instret`                                                  | 0xC82     | RO     |
| hpmcounter8h          | Upper 32 bits of `hpmcounter8`                                              | 0xC88     | RO     |
| hpmcounter9h          | Upper 32 bits of `hpmcounter9`                                              | 0xC89     | RO     |
| hpmcounter13h         | Upper 32 bits of `hpmcounter13`                                             | 0xC8D     | RO     |

Custom System CSRs (Custom)

Floating-Point User Mode CSR (Custom)
fxcr                  | Floating-point extended control register                                   | 0x800      | R/W    |

GPIO Access CSRs (Custom)
cpu_gpio_oen         | GPIO output enable                                                         | 0x803      | R/W    |
cpu_gpio_in          | GPIO input value                                                           | 0x804      | RO     |
cpu_gpio_out         | GPIO output value                                                          | 0x805      | R/W    |

Extension Control and Status CSRs (Custom)
mext_ill_reg         | Machine extension illegal register                                         | 0x7F0      | R/W    |
mhloop_state_reg     | Machine mode HWLP extension state register                                 | 0x7F1      | R/W    |
mext_pie_status      | Machine mode PIE extension status register                                 | 0x7F2      | R/W    |

Zc Extension CSRs
jvt                  | Machine table jump base vector and control register                        | 0x017      | R/W    |

Machine Extension Status CSRs (Custom)
mestatus             | Machine extension control and status register                              | 0x7E1      | R/W    |
mhint                | Machine implicit operation register                                        | 0x7C5      | R/W    |

Physical Memory Attributes Checker (PMAC) CSRs (Custom)
pma_cfgn (n: 0-15)   | Physical memory attribute configuration register                          | 0xBCO+0x1*n| R/W    |
pma_addrn (n: 0-15)  | Physical memory attribute address register                                 | 0xBDO+0x1*n| R/W    |

Machine Hardware Loop CSRs (Custom)
mhloop0_start_addr   | 32-bit start address for loop 0                                            | 0x7C6      | R/W    |
mhloop0_end_addr     | 32-bit start address for loop 0                                             | 0x7C7      | R/W    |
mhloop0_count        | Iteration count for hardware loop 0                                        | 0x7C8      | R/W    |
mhloop1_start_addr   | 32-bit start address for loop 1                                             | 0x7C9      | R/W    |
mhloop1_end_addr     | 32-bit end address for loop 1                                               | 0x7CA      | R/W    |
mhloop1_count        | Iteration count for hardware loop 1                                        | 0x7CB      | R/W    |

User Hardware Loop CSRs (Custom)
uhloop0_start_addr   | 32-bit start address for loop 0                                             | 0x8C0      | R/W    |
uhloop0_end_addr     | 32-bit end address for loop 0                                               | 0x8C1      | R/W    |
uhloop0_count        | Iteration count for hardware loop 0                                        | 0x8C2      | R/W    |
uhloop1_start_addr   | 32-bit start address for loop 1                                             | 0x8C3      | R/W    |
uhloop1_end_addr     | 32-bit end address for loop 1                                               | 0x8C4      | R/W    |
uhloop1_count        | Iteration count for hardware loop 1                                        | 0x8C5      | R/W    |
uhwloop_state_reg    | User HWLP state register                                                   | 0x8C6      | R/W    |

Bus Error Exception Context CSRs (Custom)
ldpc0                | Load bus error PC register 0                                                | 0xBE0      | R/W    |
ldpc1                | Load bus error PC register 1                                                | 0xBE1      | R/W    |
ldtval0              | Load bus error access address register 0                                   | 0xBE8      | R/W    |
ldtval1              | Load bus error access address register 1                                   | 0xBE9      | R/W    |
```