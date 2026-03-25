

```markdown
delta    A change in the program counter that is other than the difference between two instructions placed consecutively in memory  
DTM      Debug transport module  
FPR      Floating-point register  
GPIO     General-purpose input/output  
GPR      General-purpose register  
HWLP     Hardware loop  
hart     RISC-V hardware thread  
LSB      Least significant bit  
LR       Load reserved  
MSB      Most significant bit  
PMP      Physical memory protection  
retire    The final stage of executing an instruction, when the machine state is updated  
RO       Read-only field  
R/W      Readable and writable field  
SC       Store conditional  
SoC      System on chip  
WO       Write-only field  
WARL     Write any read legal  
W1       Write One  

## 2.4 Address Map

The table below shows the address map of various regions accessible by CPU for instruction, data, and system bus peripherals.

Table 2.4-1. CPU Address Map

| Region           | Description                  | Start Address   | End Address     | Access Type |
|------------------|------------------------------|-----------------|-----------------|-------------|
| CPU              | CLIC/CLINT registers         | 0x2000_0000     | 0x2FFF_FFFF     | R/W         |
| IRAM/DRAM        | Instruction/Data region       | 0x4000_0000     | 0x4FFF_FFFF     | R/W         |
| CPU peripherals  | AHB (Strong order access)     | 0x6000_0000     | 0x6FFF_FFFF     | R/W         |
| AHB              | AHB (Weak Order Access)       | *Default        | *Default        | R/W         |

*Default: Address not matching any of the specified ranges above are accessed through AHB bus by a CPU core.

## 2.5 Configuration and Status Registers (CSRs)

### 2.5.1 Register Summary

Below is a list of CSRs implemented for the HP CPU core. All the implemented CSRs follow the standard mapping of bit fields as described in the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10. It must be noted that even among the standard CSRs, not all bit fields have been implemented,
```