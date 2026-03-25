

```markdown
Figure 44.1-1. BitScrambler System Context Diagram
```

## 44.2 Feature List

The BitScrambler has the following features:

*   One BitScrambler core, which can be used as either a RX (peripheral-to-memory), or TX (memory-to-peripheral) unit
*   Support for memory-to-memory transfers
*   Processing up to 32 bits per DMA clock period
*   Data path controlled by a BitScrambler program stored in instruction memory
*   Input registers able to read 0, 8, 16, or 32 bits per clock cycle

    *   Output registers:
        *   Able to write 0, 8, 16, or 32 bits per clock cycle
            *   Data sources for output register bits: 64 bits of input data, two counters, LUT RAM data, data output of last cycle, comparators
            *   With some restrictions, each of the 32 output register bits can come from any bit on the data sources

*   8 x 257-bit instruction memory, for storing eight instructions, controlling control flow and the data path
*   2048 bytes of lookup table (LUT) memory, configurable as various word widths

## 44.3 Application Examples

*   Swapping byte, nibble or bit orders in data
*   Converting palette-based bitmaps to full RGB bitmaps
*   Run-length encoding or decoding of data
*   Generating complicated waveforms for e.g. WS2811 chips
```