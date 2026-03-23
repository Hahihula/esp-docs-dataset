

```markdown
## 30.4 System Architecture

Figure 30.4-1 shows the structure of ESP32-C6 I2S module, consisting of:

* Transmit control unit (TX Unit)
* Receive control unit (RX Unit)
* Input and output timing unit (I/O Sync)
* Clock divider (Clock Generator)
* 64 x 32-bit TX FIFO
* 64 x 32-bit RX FIFO
* Compress/Decompress units

I2S module supports direct memory access (DMA) to internal memory. For more information, see Chapter 4 GDMA Controller (GDMA).

Both the TX unit and the RX unit have a three-line interface that uses a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the TX unit is fixed as output, and the SD line of the RX unit as input. BCK and WS signal lines for TX unit and RX unit can be configured as master output mode or slave input mode.

The signal bus of I2S module is shown at the right part of Figure 30.4-1. The naming of these signals in RX and TX units follows the pattern: `I2S_A_B_C`, such as `I2SI_BCK_in`.

* “A” represents the direction of data bus, which includes:

    - “I”: input, receiving
```