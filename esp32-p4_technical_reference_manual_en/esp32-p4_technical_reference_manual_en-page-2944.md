

```markdown
Figure 59.1-1. BitScrambler System Context Diagram

59.2 Feature List

The BitScrambler has the following features:

*   Two BitScramblers, one for RX (peripheral-to-memory), one for TX (memory-to-peripheral)
*   Support for memory-to-memory transfers
*   Processing up to 32 bits per DMA clock period
*   Data path controlled by a BitScrambler program stored in instruction memory
*   Input registers able to read 0, 8, 16, or 32 bits per clock cycle

Output registers:

    - Able to write 0, 8, 16, or 32 bits per clock cycle
    - Data sources for output register bits: 64 bits of input data, two counters, LUT RAM data, data output of last cycle, comparators
    - With some restrictions, each of the 32 output register bits can come from any bit on the data sources

*   8 x 257-bit instruction memory, for storing eight instructions, controlling control flow and the data path
*   2048 bytes of lookup table (LUT) memory, configurable as various word widths

59.3 Architectural Overview

The BitScrambler can be separated into a data path, a control path, and the registers that the CPU can use to program them. The data path moves bits between the incoming DMA stream, internal registers, and the outgoing DMA stream. The control path parses the instructions in the instruction memory to control the data path, as well as handle program flow.
```