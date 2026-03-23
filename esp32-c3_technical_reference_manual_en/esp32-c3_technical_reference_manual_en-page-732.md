

```markdown
## 29.4 System Architecture

Figure 29.4-1 shows the structure of ESP32-C3 I2S module, consisting of:

*   TX unit (TX control)
*   RX unit (RX control)
*   input and output timing unit (I/O sync)
*   clock divider (Clock Generator)
*   64 x 32-bit TX FIFO
*   64 x 32-bit RX FIFO
*   Compress/Decompress units

I2S module supports direct access (DMA) to internal memory, see Chapter 2 GDMA Controller (GDMA).

Both the TX unit and the RX unit have a three-line interface that includes a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the TX unit is fixed as output, and the SD line of the RX unit as input. BCK and WS signal lines for TX unit and RX unit can be configured as master output mode or slave input mode.

The signal bus of I2S module is shown at the right part of Figure 29.4-1. The naming of these signals in RX and TX units follows the pattern: `I2SA_B_C`, such as `I2SI_BCK_in`.

*   “A”: direction of data bus
    *   – “I”: input, receiving
    *   – “O”: output, transmitting
```