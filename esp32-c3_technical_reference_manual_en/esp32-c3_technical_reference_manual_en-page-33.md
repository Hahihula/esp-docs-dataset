

```markdown
| Name               | Description                                | Address | Access |
|--------------------|--------------------------------------------|---------|--------|
| mstatus            | Machine Mode Status                        | 0x300   | R/W    |
| misa¹              | Machine ISA                                | 0x301   | R/W    |
| mtvec²             | Machine Trap Vector                        | 0x305   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **Machine Trap Handling CSRs** |                                    |         |        |
| mscratch           | Machine Scratch                            | 0x340   | R/W    |
| mepc               | Machine Trap Program Counter               | 0x341   | R/W    |
| mcause³            | Machine Trap Cause                         | 0x342   | R/W    |
| mtval              | Machine Trap Value                         | 0x343   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **Physical Memory Protection (PMP) CSRs** |                                    |         |        |
| pmpcfg0            | Physical memory protection configuration  | 0x3A0   | R/W    |
| pmpcfg1            | Physical memory protection configuration  | 0x3A1   | R/W    |
| pmpcfg2            | Physical memory protection configuration  | 0x3A2   | R/W    |
| pmpcfg3            | Physical memory protection configuration  | 0x3A3   | R/W    |
| pmpaddr0           | Physical memory protection address register | 0x3B0   | R/W    |
| pmpaddr1           | Physical memory protection address register | 0x3B1   | R/W    |
|                    | ....                                      |         |        |
| pmpaddr15          | Physical memory protection address register | 0x3BF   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **Trigger Module CSRs (shared with Debug Mode)** |                                    |         |        |
| tselect            | Trigger Select Register                    | 0x7A0   | R/W    |
| tdata1             | Trigger Abstract Data 1                    | 0x7A1   | R/W    |
| tdata2             | Trigger Abstract Data 2                    | 0x7A2   | R/W    |
| tcontrol           | Global Trigger Control                     | 0x7A5   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **Debug Mode CSRs** |                                    |         |        |
| dcsr               | Debug Control and Status                   | 0x7B0   | R/W    |
| dpc                | Debug PC                                   | 0x7B1   | R/W    |
| dscratch0          | Debug Scratch Register 0                   | 0x7B2   | R/W    |
| dscratch1          | Debug Scratch Register 1                   | 0x7B3   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **Performance Counter CSRs (Custom)⁴** |                                    |         |        |
| mpcer              | Machine Performance Counter Event          | 0x7E0   | R/W    |
| mpcmr              | Machine Performance Counter Mode           | 0x7E1   | R/W    |
| mpccr              | Machine Performance Counter Count          | 0x7E2   | R/W    |
|--------------------|--------------------------------------------|---------|--------|
| **GPIO Access CSRs (Custom)** |                                    |         |        |
| cpu_gpio_oen       | GPIO Output Enable                         | 0x803   | R/W    |
| cpu_gpio_in        | GPIO Input Value                           | 0x804   | RO     |
| cpu_gpio_out       | GPIO Output Value                          | 0x805   | R/W    |
```

Note that if write/set/clear operation is attempted on any of the CSRs which are read-only (RO), as indicated in the above table, the CPU will generate illegal instruction exception.

¹Although `misa` is specified as having both read and write access (R/W), its fields are hardwired and thus write has no effect. This is what would be termed WARL (Write Any Read Legal) in RISC-V terminology  
²`mtvec` only provides configuration for trap handling in vectored mode with the base address aligned to 256 bytes  
³External interrupt IDs reflected in `mcause` include even those IDs which have been reserved by RISC-V standard for core internal sources.  
⁴These custom CSRs have been implemented in the address space reserved by RISC-V standard for custom use
```