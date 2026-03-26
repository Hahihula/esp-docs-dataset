

```markdown
Chapter 1 High-Performance CPU

GoBack

1.2 Features

Each RISC-V CPU core in the CPU core complex implements the following standard RISC-V extensions:

* Mandatory base integer (I)
* Multiplication/Division (M)
* Atomic (A)
* Floating (F)
* Compressed (C)
* Code size reduction (Zc)
* Bit Manipulation (Zb)

In addition to the above standard extensions, each RISC-V CPU core also implements custom instructions (X) which can be broadly classified in the following two categories:

* Custom instructions to accelerate AI algorithms performance
* Custom hardware loop instructions to further improve performance and reduce code size for iterative AI algorithms execution

Apart from the above RISC-V instruction extensions support, each CPU core supports the features below:

* RISC-V RV32IMAFXC ISA with a five-stage pipeline that supports an operating clock frequency up to 360 MHz
* Compatible with RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2
* Compatible with RISC-V Instruction Set Manual, Volume II: RISC-V Privileged Architecture, Version 1.10
* Compatible with Core-Local Interrupt Controller (CLIC) RISC-V Privileged Architecture Extensions (10/10/2023)
* Compatible with RISC-V External Debug Support Version 0.13.2
* Zero wait cycle access to on-chip SRAM and cache for program and data access over IRAM/DRAM interface
* 32-bit AHB system bus for peripheral access
* Core-local interrupts (CLINT) dedicated for each privilege mode
* User (U) privilege mode execution
* Interrupt delegation to user mode
* Bus error response
* Standard physical memory protection (PMP) configurable up to 32 regions and custom attributes (PMA) configurable up to 16 regions for security
* Branch target buffer (BTB) with BHT and RAS for performance improvement
* Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13.2 with external debugger support over an industry-standard JTAG/USB port

Espressif Systems
62
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```