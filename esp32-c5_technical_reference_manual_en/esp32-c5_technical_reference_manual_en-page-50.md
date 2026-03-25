

```markdown
- Multiplication/Division (M)
- Atomic (A)
- Compressed (C)
- Code size reduction (Zc)

Apart from the above RISC-V instruction extensions support, the CPU core supports the features below:

- Five-stage pipeline that supports an operating clock frequency up to 360 MHz
- Compatible with RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2
- Compatible with RISC-V Instruction Set Manual, Volume II: RISC-V Privileged Architecture, Version 1.10
- Compatible with RISC-V Core-Local Interrupt Controller (CLIC) Version 0.9
- Compatible with RISC-V External Debug Support Version 0.13.2
- Zero wait cycle access to on-chip SRAM and cache for program and data access over IRAM/DRAM interface

- 32-bit AHB system bus for peripheral access
- Core-local interrupts (CLINT)
- User (U) privilege mode execution
- Bus error response
- Standard physical memory protection (PMP) and custom attributes (PMA) for up to 16 configurable regions for security
- Branch target buffer (BTB) with BHT and RAS for performance improvement
- Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13.2 with external debugger support over an industry-standard JTAG/USB port
- Debugger with a direct system bus access (SBA) to memory and peripherals via the core data bus
- Support for instruction trace for offline debug
- Hardware trigger compliant with the specification RISC-V External Debug Support Version 0.13.2 with up to 3 breakpoints/watchpoints
- Support for up to 8 dedicated IOs
- Configurable events for core performance metrics

## 2.3 Terminology

To better illustrate the functionality of the ESP-RISC-V CPU, the following terms are used in this chapter.

| Term | Definition |
|------|------------|
| ABI | Application binary interface |
| branch | An instruction that conditionally changes the execution flow |
| CLIC | Core-local interrupt controller |
| CLINT | Core-local interrupt |
| CSR | Control and status register |
```