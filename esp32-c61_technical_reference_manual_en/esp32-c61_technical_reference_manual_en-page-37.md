

```markdown
|branch|An instruction that conditionally changes the execution flow|
|:-------|:------------------------------------------------------------------------------------------------------------------------|
|CLIC|Core-local interrupt controller|
|CLINT|Core-local interrupt|
|CSR|Control and status register|
|delta|A change in the program counter that is other than the difference between two instructions placed consecutively in memory|
|DTM|Debug transport module|
|FPR|Floating-point register|
|GPIO|General-purpose input/output|
|GPR|General-purpose register|
|HWLP|Hardware loop|
|hart|RISC-V hardware thread|
|LSB|Least significant bit|
|LR|Load reserved|
|MSB|Most significant bit|
|PMP|Physical memory protection|
|retire|The final stage of executing an instruction, when the machine state is updated|
||Read-only field|
|R/W|Readable and writable field|
|SC|Store conditional|
|SoC|System on chip|
|WO|Write-only field|
|WARL|Write any read legal|
|W1|Write One|

## 1.4 Address Map

The table below shows the address map of various regions accessible by CPU for instruction, data, and system bus peripherals.

Table 1.4-1. CPU Address Map

<table><thead><tr><td>Region</td><td>Description</td><td>Start Address</td><td>End Address</td><td>Access Type</td></tr></thead><tbody><tr><td>CPU</td><td>CLIC/CLINT registers</td><td>0x2000_0000</td><td>0x2FFF_FFFF</td><td>R/W</td></tr><tr><td>IRAM/DRAM</td><td>Instruction/Data region</td><td>0x4000_0000</td><td>0x4FFFF_FFFF</td><td>R/W</td></tr><tr><td>CPU peripherals</td><td>AHB (Strong order access)</td><td>0x6000_0000</td><td>0x6FFFF_FFFF</td><td>R/W</td></tr><tr><td>AHB</td><td>AHB (Weak Order Access)</td><td>*Default</td><td>*Default</td><td>R/W</td></tr></tbody></table>

*Default*: Address not matching any of the specified ranges above are accessed through AHB bus by a CPU core.

## 1.5 Configuration and Status Registers (CSRs)
```