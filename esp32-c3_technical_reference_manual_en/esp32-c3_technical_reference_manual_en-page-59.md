

```markdown
| Name          | Description                                                      | Address | Access |
|---------------|------------------------------------------------------------------|---------|--------|
| pmcfg0        | Physical memory protection configuration.                        | 0x3A0   | R/W    |
| pmcfg1        | Physical memory protection configuration.                        | 0x3A1   | R/W    |
| pmcfg2        | Physical memory protection configuration.                        | 0x3A2   | R/W    |
| pmcfg3        | Physical memory protection configuration.                        | 0x3A3   | R/W    |
| pmpaddr0      | Physical memory protection address register.                     | 0x3B0   | R/W    |
| pmpaddr1      | Physical memory protection address register.                     | 0x3B1   | R/W    |
| pmpaddr2      | Physical memory protection address register.                     | 0x3B2   | R/W    |
| pmpaddr3      | Physical memory protection address register.                     | 0x3B3   | R/W    |
| pmpaddr4      | Physical memory protection address register.                     | 0x3B4   | R/W    |
| pmpaddr5      | Physical memory protection address register.                     | 0x3B5   | R/W    |
| pmpaddr6      | Physical memory protection address register.                     | 0x3B6   | R/W    |
| pmpaddr7      | Physical memory protection address register.                     | 0x3B7   | R/W    |
| pmpaddr8      | Physical memory protection address register.                     | 0x3B8   | R/W    |
| pmpaddr9      | Physical memory protection address register.                     | 0x3B9   | R/W    |
| pmpaddr10     | Physical memory protection address register.                     | 0x3BA   | R/W    |
| pmpaddr11     | Physical memory protection address register.                     | 0x3BB   | R/W    |
| pmpaddr12     | Physical memory protection address register.                     | 0x3BC   | R/W    |
| pmpaddr13     | Physical memory protection address register.                     | 0x3BD   | R/W    |
| pmpaddr14     | Physical memory protection address register.                     | 0x3BE   | R/W    |
| pmpaddr15     | Physical memory protection address register.                     | 0x3BF   | R/W    |
```

### 1.8.4 Register Summary

Below is a list of PMP CSRs supported by the CPU. These are only accessible from machine-mode.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

### 1.8.5 Register Description

PMP unit implements all pmcfg0-3 and pmpaddr0-15 CSRs as defined in RISC-V Instruction Set Manual Volume II: Privileged Architecture, Version 1.10.
```