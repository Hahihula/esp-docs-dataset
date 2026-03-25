

```markdown
- ETM feature
- Direct Memory Access
- Standard I2S interface interrupts

Note:
In slave mode, due to the frequency limitation of the clock source, the maximum sampling frequency of the ESP32-H2 I2S is limited by the data bit width and the number of channels. For example, sampling frequencies up to 187.5 kHz (such as 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, and 128 kHz) are supported in 32-bit two-channel sampling. Please refer to Section 31.6 for detailed information.
```

## 31.4 System Architecture

Figure 31.4-1 shows the structure of the ESP32-H2 I2S module, consisting of:

- Transmit control unit (TX Unit)
- Receive control unit (RX Unit)
- Input and output timing unit (I/O Sync)
- Clock divider (Clock Generator)
- 64 x 32-bit TX FIFO
- 64 x 32-bit RX FIFO
- Compress/Decompress units

Figure 31.4-1. ESP32-H2 I2S System Diagram
```