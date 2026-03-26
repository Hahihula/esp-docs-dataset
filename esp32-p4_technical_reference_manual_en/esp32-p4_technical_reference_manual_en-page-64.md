

```markdown
| Region          | Description                          | Start Address   | End Address     | Access Type |
|-----------------|--------------------------------------|-----------------|-----------------|-------------|
| CPU             | CLIC/CLINT registers                 | 0x2000_0000     | 0x2FFF_FFFF     | R/W         |
| IRAM/DRAM       | Instruction/Data region              | 0x3000_0000     | 0x3FEF_FFFF     | R/W         |
| CPU peripherals |                                      | 0x3FF0_0000     | 0x3FF1_FFFF     | R/W         |
| IRAM/DRAM       | Instruction/Data region              | 0x3FF2_0000     | 0x4FFFF_FFFF    | R/W         |
| CPU peripherals | HP APB peripherals                   | 0x5000_0000     | 0x500F_FFFF     | R/W         |
| LP RAM/ROM      |                                      | 0x5010_0000     | 0x5010_FFFF     | R/W         |
| LP APB peripherals |                                  | 0x5011_0000     | 0x5012_FFFF     |             |
| AHB             | AHB peripheral region                | *Default        | *Default        | R/W         |

*Default: Addresses not matching any of the specified ranges above are accessed through AHB bus by a CPU core.

## 1.5 Configuration and Status Registers (CSRs)

### 1.5.1 Register Summary

Below is a list of CSRs implemented for each HP CPU core. All the implemented CSRs follow the standard mapping of bit fields as described in the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. It must be noted that even among the standard CSRs, not all bit fields have been implemented, limited by the subset of features implemented in the CPU. Refer to the next section for detailed description of the subset of fields implemented under each of these CSRs.

| Name                         | Description                                                                                   | Address | Access |
|------------------------------|-----------------------------------------------------------------------------------------------|---------|--------|
| **Machine Information CSRs** |                                                                                               |         |        |
| mvendorid                    | Machine vendor ID                                                                             | 0xF11   | RO     |
| marchid                      | Machine architecture ID                                                                       | 0xF12   | RO     |
| mimpid                       | Machine implementation ID                                                                     | 0xF13   | RO     |
| mhartid                      | Machine hart ID                                                                               | 0xF14   | RO     |
| **Machine Trap Setup CSRs**  |                                                                                               |         |        |
| mstatus                      | Machine mode status                                                                           | 0x300   | R/W    |
| misa¹                        | Machine ISA                                                                                  | 0x301   | R/W    |
| mideleleg                    | Machine interrupt delegation register (INACTIVE IN CLIC MODE)                               | 0x303   | RO     |
| mie                          | Machine interrupt enable register (INACTIVE IN CLIC MODE)                                   | 0x304   | RO     |
| mtvec²                       | Machine trap vector                                                                          | 0x305   | R/W    |
| mcounteren                   | Machine counter enable                                                                       | 0x306   | R/W    |
| mtvt                         | Machine vector interrupt base address (Refer to CLIC specifications)                        | 0x307   | R/W    |

¹Although misa is specified as having both read and write access (R/W), its fields are hardwired and thus write has no effect. This is what would be termed WARL (Write Any Read Legal) in RISC-V terminology
²mtvec Holds trap vector configuration consisting of vector base address and a vector mode
```