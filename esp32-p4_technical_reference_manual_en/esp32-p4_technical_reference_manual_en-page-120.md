

```markdown
Chapter 1 High-Performance CPU

GoBack

1.7.2 Processor Instruction Extension

1.7.2.1 Overview

The Processor Instruction Extension (PIE) ISA entails various custom 128-bit wide SIMD (Single Instruction Multiple Data) and complex instructions for accelerating edge inference and digital signal processing applications. These instructions are fully integrated into the CPU pipeline for seamless use with the standard RV32IMAFCA ISA with which the HP core is compliant. PIE Extension support is compliant to Espressif’s PIE V2.2.0 version.

1.7.2.2 Functional Description

- 8 x 128-bit wide integer vector register files
- Each 128-bit wide vector register can be used as 16 x 8-bit elements, 8 x 16-bit elements, or 4 x 32-bit elements for SIMD operations
- Up to 128-bit wide memory load/store operations directly to/from the vector registers
- Fused instructions for parallel execution of arithmetic and memory operations
- Vector and scalar MAC units capable of operating on 16 x 8-bit elements or 8 x 16-bit elements per cycle
- 512-bit wide vector register for accumulating results of 8/16-bit vector MAC operations
- 40-bit wide scalar register for accumulating results of 8/16-bit scalar MAC operations
- Instructions for parallel 16-bit FFT/complex math operations
- Final results are generated after rounding and saturation
- Configurable rounding modes and scaling (arithmetic right shift) parameter

For a complete description of all the available instructions and configurations, please refer to Chapter 2 Processor Instruction Extensions [to be added later].

1.7.2.3 Initialization, Context Switching, and Exceptions

The PIE extension is disabled by default and must be manually enabled using the next_pie_status.STATE field. Otherwise, an illegal instruction exception will be generated upon executing any of the instructions that are part of the PIE extension.

To indicate that an illegal instruction exception, i.e. exception with mcause = 0x2, has occurred due to disabled PIE extension, the HP core will set the next_ill.PIE_ILL bit.

When the PIE extension is enabled, i.e. next_pie_status.STATE bits are non-zero, the execution of any PIE instructions would always cause the next_pie_status.STATE bits to change to DIRTY (11).

To enable the PIE extension, follow the steps below:

1. Set the next_pie_status.STATE bits to the INITIAL (01) state.
2. Use the PIE instructions to initialize the PIE register file and accumulator registers to zero, which will cause the next_pie_status.STATE bits to change to DIRTY (11) automatically.
3. Since the value of the PIE registers is known at this point, set the next_pie_status.STATE bits to CLEAN (10).

Espressif Systems
```