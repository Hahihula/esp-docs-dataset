

```markdown
- PDM TX mode
  * Raw PDM data transmission
  * PCM-to-PDM data format conversion (for I2S0 only), up to 2 channels supported
- PDM RX mode
  * Raw PDM data reception
  * PDM-to-PCM data format conversion (for I2S0 only), up to 8 channels supported

• Configurable APLL clock with frequencies up to 240 MHz
• Configurable high-precision sample clock with a variety of sampling frequencies supported (refer to the note below for more details)
• 8/16/24/32-bit data width
• Synchronous counter in TX mode
• ETM feature
• Direct Memory Access (GDMA-AHB only)
• Standard I2S interface interrupts

Note:
In slave mode, to ensure the sampling accuracy, the module clock frequency must be greater than or equal to 8 times the BCK clock frequency. Therefore, the maximum sampling frequency of I2Sn is limited by the data bit width and the number of channels. For example, since the clock source frequency is up to 240 MHz, the module clock can be configured up to 120 MHz, and the BCK clock can be configured up to 15 MHz. Therefore, when transmitting dual-channel 32-bit width data, I2Sn supports sample frequencies up to 234.375 kHz, e.g., 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, and 192 kHz. Please refer to Section 46.6 I2S TX/RX Clock for detailed information.
```

## 46.4 System Architecture

Figure 46.4-1 shows the structure of the ESP32-P4 I2Sn module, consisting of:

* Transmit control unit (TX Unit)
* Receive control unit (RX Unit)
* Input and output timing unit (I/O Sync)
* Clock divider (Clock Generator)
* 64 x 32-bit TX FIFO
* 64 x 32-bit RX FIFO
* Compress/Decompress units
```