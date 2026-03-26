

```markdown
- Standard LP I2S interface interrupts

## 47.3 Architectural Overview

Figure 47.3-1 shows the structure of the ESP32-P4 LP I2S module, consisting of:

- Receive control unit (RX Unit)
- Input and output timing unit (I/O Sync)
- Clock divider (Clock Generator)
- 64 x 32-bit RX FIFO
- 256 x 32-bit LP I2S Memory
- Communication interface for Voice Activity Detection (VAD)

![Figure 47.3-1. ESP32-P4 LP I2S Architecture](image_path_if_available)

**Figure 47.3-1. ESP32-P4 LP I2S Architecture**

The RX unit have a three-line interface that uses a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the RX unit is dedicated for data input. BCK and WS signal lines for the RX unit can be configured as master output mode or slave input mode.

The signal bus of the LP I2S module is shown at the right part of Figure 47.3-1. The naming of these signals in RX units follows the pattern of `LP_I2SA_B_C`, for example, `LP_I2SI_BCK_in`.

- “A” is fixed to “I”, indicating that signals are input to the RX unit
- “B” represents the signal function, which includes:

  - BCK
```