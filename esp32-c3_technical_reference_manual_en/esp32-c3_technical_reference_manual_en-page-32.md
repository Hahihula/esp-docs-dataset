

```markdown
- Debug module (DM) compliant with RISC-V debug specification v0.13 with external debugger support over an industry-standard JTAG/USB port
- Debugger direct system bus access (SBA) to memory and peripherals
- Hardware trigger compliant to RISC-V debug specification v0.13 with up to 8 breakpoints/watchpoints
- Physical memory protection (PMP) for up to 16 configurable regions
- 32-bit AHB system bus for peripheral access
- Configurable events for core performance metrics

## 1.3 Address Map

Below table shows address map of various regions accessible by CPU for instruction, data, system bus peripheral and debug.

Table 1.3-1. CPU Address Map

| Name   | Description               | Starting Address | Ending Address    | Access |
|--------|---------------------------|------------------|-------------------|--------|
| IRAM   | Instruction Address Map   | 0x4000_0000      | 0x47FF_FFFF       | R/W    |
| DRAM   | Data Address Map          | 0x3800_0000      | 0x3FFF_FFFF       | R/W    |
| DM     | Debug Address Map         | 0x2000_0000      | 0x27FF_FFFF       | R/W    |
| AHB    | AHB Address Map           | *default         | *default          | R/W    |

*default : Address not matching any of the specified ranges (IRAM, DRAM, DM) are accessed using AHB bus.

## 1.4 Configuration and Status Registers (CSRs)

### 1.4.1 Register Summary

Below is a list of CSRs available to the CPU. Except for the custom performance counter CSRs and the tcontrol register (which complies with the RISC-V External Debug Support Version 0.13.2), all the implemented CSRs follow the standard mapping of bit fields as described in the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. It must be noted that even among the standard CSRs, not all bit fields have been implemented, limited by the subset of features implemented in the CPU. Refer to the next section for detailed description of the subset of fields implemented under each of these CSRs.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                  | Description                                                                 | Address | Access |
|-----------------------|-----------------------------------------------------------------------------|---------|--------|
| **Machine Information CSRs** |                                                                 |         |        |
| mvendorid             | Machine Vendor ID                                                           | 0xF11   | RO     |
| marchid               | Machine Architecture ID                                                    | 0xF12   | RO     |
| mimpid                | Machine Implementation ID                                                  | 0xF13   | RO     |
| mhartid               | Machine Hart ID                                                             | 0xF14   | RO     |
| **Machine Trap Setup CSRs**    |                                                                 |         |        |
```