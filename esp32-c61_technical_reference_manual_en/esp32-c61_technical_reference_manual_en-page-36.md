

```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

• Mandatory base integer (I)
• Multiplication/Division (M)
• Atomic (A)
• Compressed (C)
• Code size reduction (Zc)
• Bit manipulation (Zb)

Apart from the above RISC-V instruction extensions support, CPU core supports the features below:

• Five-stage pipeline that supports an operating clock frequency up to 160 MHz
• Compatible with RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2
• Compatible with RISC-V Instruction Set Manual, Volume II: RISC-V Privileged Architecture, Version 1.10
• Compatible with RISC-V Core-Local Interrupt Controller (CLIC) Version 0.9
• Compatible with RISC-V External Debug Support Version 0.13.2

• Zero wait cycle access to on-chip SRAM and cache for program and data access over IRAM/DRAM interface
• 32-bit AHB system bus for peripheral access
• Core-local interrupts (CLINT) support
• User (U) privilege mode execution
• User (U) mode interrupt delegation via CLIC

• Bus error response
• Standard physical memory protection (PMP) and custom attributes (PMA) for up to 16 configurable regions for security
• Branch target buffer (BTB) with BHT and RAS for performance improvement
• Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13.2 with external debugger support over an industry-standard JTAG/USB port
• Debugger with a direct system bus access (SBA) to memory and peripherals via Core 0 data bus
• Support for instruction trace for offline debug
• Hardware trigger compliant with the specification RISC-V External Debug Support Version 0.13.2 with up to 3 breakpoints/watchpoints
• Support for up to 8 dedicated IOs
• Configurable events for core performance metrics

1.3 Terminology

To better illustrate the functionality of ESP-RISC-V CPU, the following terms are used in this chapter.

ABI Application binary interface

Espressif Systems                           36                          ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback               PRELIMINARY
```