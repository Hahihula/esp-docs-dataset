

```markdown
Chapter 1 High-Performance CPU

1.6.3 F Extension

1.6.3.1 Overview

Each HP core implements the RISC-V standard single-precision floating-point instruction set extension, "RV32F" extension in short. The RV32F extension also provides its own register file and various CSRs for configuration and flag checking. Please refer to the RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2, F Standard Extension Version 2.0" for complete information.

1.6.3.2 Functional Description

- Various instructions to perform floating-point arithmetic operations, conversion/move operations to/from integer format, comparison operations, classification operations, and memory load/store operations.
- Single-precision 32-bit floating-point operations compliant with IEEE 754-2008 standard.
- Separate 32-bit wide floating-point register file with 32 registers.
- Configurable rounding modes.
- Flags for checking inexact, overflow, underflow, invalid and divide by zero outcomes.
- Subnormal and NaN (not a number) arithmetic
- Status bits to control the availability of the extension and track its usage in the context of a program execution.

1.6.3.3 Initialization

The RV32F extension is disabled by default and must be manually enabled using the mstatus.FS bits. Otherwise, an illegal instruction exception will be generated upon executing any of the instructions, or accessing any of the CSRs, which are part of the RV32F extension.

Please refer to the RISC-V Instruction Set Manual, Volume II: Privileged Architecture, Version 1.10, Extension Context Status in mstatus Register for complete information.
```