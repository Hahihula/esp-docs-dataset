

```markdown
Figure 46.4-1. ESP32-P4 I2S System Diagram

Note: The PDM-to-PCM converter and PCM-to-PDM converter are only supported by I2S0.
```

The I2Sn module supports direct memory access (DMA) to internal memory. For more information, see Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).

Both the TX unit and the RX unit have a three-line interface that uses a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the TX unit is used for data output and the SD line of the RX unit for data input. The BCK and WS signal lines of the TX and RX units are used for data output in master mode, and the BCK and WS signal lines of the TX and RX units are used for data input in slave mode.

The signal bus of the I2Sn module is shown at the right part of Figure 46.4-1. The naming of these signals in RX and TX units follows the pattern of I2SnA_B_C such as I2SnI_BCK_in.

*   "A" indicates that the signal belongs to the I2Sn TX or RX unit, which includes:
    *   "I": Signal input to/output from the RX unit
    *   "O": Signal input to/output from the TX unit
*   "B" represents the signal function, which includes:
    *   BCK
    *   WS
    *   SD
*   "C" represents the signal direction, which includes:
    *   "in": Input signal into the I2Sn module
    *   "out": Output signal from the I2Sn module

Espressif Systems

ESP32-P4 TRM
PRELIMINARY
```