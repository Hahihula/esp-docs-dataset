

```markdown
| Name                         | Description                          | Address | Access |
|------------------------------|--------------------------------------|---------|--------|
| **Machine Information CSRs** |                                      |         |        |
| mvvendorid                   | Machine Vendor ID                    | 0xF11   | RO     |
| marchid                      | Machine Architecture ID              | 0xF12   | RO     |
| mimpid                       | Machine Implementation ID            | 0xF13   | RO     |
| mhartid                      | Machine Hart ID                      | 0xF14   | RO     |
| **Machine Trap Setup CSRs**  |                                      |         |        |
| mstatus                      | Machine Mode Status                  | 0x300   | R/W    |
| misa¹                        | Machine ISA                          | 0x301   | R/W    |
| mideleleg                    | Machine Interrupt Delegation Register| 0x303   | R/W    |
| mie                          | Machine Interrupt Enable Register    | 0x304   | R/W    |
| mtvec²                       | Machine Trap Vector                  | 0x305   | R/W    |
| **Machine Trap Handling CSRs**|                                      |         |        |
| mscratch                     | Machine Scratch                      | 0x340   | R/W    |
| mepc                         | Machine Trap Program Counter         | 0x341   | R/W    |
| mcause³                      | Machine Trap Cause                   | 0x342   | R/W    |
| mtval                        | Machine Trap Value                   | 0x343   | R/W    |
| mip                          | Machine Interrupt Pending            | 0x344   | R/W    |
| **User Trap Setup CSRs**     |                                      |         |        |
| ustatus                      | User Mode Status                     | 0x000   | R/W    |
| uie                           | User Interrupt Enable Register       | 0x004   | R/W    |
| utvec                        | User Trap Vector                     | 0x005   | R/W    |
| **User Trap Handling CSRs**  |                                      |         |        |
| uscratch                     | User Scratch                         | 0x040   | R/W    |
| uepc                         | User Trap Program Counter            | 0x041   | R/W    |
| ucause                       | User Trap Cause                      | 0x042   | R/W    |
| uip                           | User Interrupt Pending               | 0x044   | R/W    |
| **Physical Memory Protection (PMP) CSRs** |                                      |         |        |
| pmpcfg0                      | Physical memory protection configuration | 0x3A0   | R/W    |
| pmpcfg1                      | Physical memory protection configuration | 0x3A1   | R/W    |
| pmpcfg2                      | Physical memory protection configuration | 0x3A2   | R/W    |
```