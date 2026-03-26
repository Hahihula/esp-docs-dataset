

```markdown
- Debugger with a direct system bus access (SBA) to memory and peripherals via Core 0 data bus
- Support for instruction trace for offline debug
- Hardware trigger compliant with the specification RISC-V External Debug Support Version 0.13.2 with up to 3 breakpoints/watchpoints
- Fast GPIO support (up to 8)
- Configurable events for core performance metrics

## 1.3 Terminology

To better illustrate the functionality of the High-Performance CPU, the following terms are used in this chapter.

| Term | Definition |
|------|------------|
| ABI | Application binary interface |
| branch | An instruction that conditionally changes the execution flow |
| CLIC | Core-local interrupt controller |
| CLINT | Core-local interrupt |
| CSR | Control and status register |
| delta | A change in the program counter that is other than the difference between two instructions placed consecutively in memory |
| DTM | Debug transport module |
| FPR | Floating-point register |
| GPIO | General-purpose input/output |
| GPR | General-purpose register |
| HWLP | Hardware loop |
| hart | RISC-V hardware thread |
| LSB | Least significant bit |
| LR | Load reserved |
| MSB | Most significant bit |
| PMP | Physical memory protection |
| retire | The final stage of executing an instruction, when the machine state is updated |
| RO | Read-only field |
| R/W | Readable and writable field |
| SC | Store conditional |
| SoC | System on chip |
| WO | Write-only field |
| WARL | Write any read legal |
| W1 | Write One |

## 1.4 Address Map

The table below shows the address map of various regions accessible by CPU for instruction, data, and system bus peripherals.
```