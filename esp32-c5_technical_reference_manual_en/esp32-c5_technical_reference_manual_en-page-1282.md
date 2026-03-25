

```markdown
Figure 35.4-1. ESP32-C5 I2S System Diagram

The I2S module supports direct memory access (DMA) to internal memory. For more information, see Chapter 5 GDMA Controller (GDMA).

Both the TX unit and the RX unit have a three-line interface that uses a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the TX unit is used for data output and the SD line of the RX unit for data input. The BCK and WS signal lines of the TX and RX units are used for data output in master mode, and the BCK and WS signal lines of the TX and RX units are used for data input in slave mode.

The signal bus of the I2S module is shown at the right part of Figure 35.4-1. The naming of these signals in RX and TX units follows the pattern of I2SA_B_C such as I2SI_BCK_in.

*   "A" indicates that the signal belongs to the I2S TX or RX unit, which includes:
    -   "I": Signal input to/output from the RX unit
        -   "O": Signal input to/output from the TX unit
*   "B" represents the signal function, which includes:
    -   BCK
    -   WS
    -   SD
*   "C" represents the signal direction, which includes:
    -   "in": Input signal into the I2S module
    -   "out": Output signal from the I2S module

Table 35.4-1 provides a detailed description of I2S signals.
```