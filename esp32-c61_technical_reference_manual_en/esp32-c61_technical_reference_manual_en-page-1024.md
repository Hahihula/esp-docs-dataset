

```markdown
- ETM feature
- Direct Memory Access
- Standard I2S interface interrupts


Note:
In slave mode, due to the frequency limitation of the clock source, the maximum sampling frequency of the ESP32-C61 I2S is limited by the data bit width and the number of channels. For example, sampling frequencies up to 312.5 kHz (such as 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, and 256 kHz) are supported in 32-bit two-channel sampling. Please refer to Section 28.6 for detailed information.
```