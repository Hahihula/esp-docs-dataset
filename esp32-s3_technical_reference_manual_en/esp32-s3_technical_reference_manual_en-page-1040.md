**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**GoBack Link:** GoBack

**List of Features and Specifications in Chapter 28:**
- PDM TX mode
- PDM RX mode
- PCM-to-PDM TX mode (for I2SO only)
- PDM-to-PCM RX mode (for I2SO only)
- Configurable high-precision sample clock
- Various frequencies supported: 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, and 192 kHz (192 kHz is not supported in 32-bit slave mode).
- 8-/16-/24-/32-bit data communication
- DMA access
- Standard I2S interface interrupts

**Section Title:**
28.4 System Architecture

**Figure Description and Caption for Figure 28.4-1 ESP32-S3 I2S System Diagram (Note: PDM-to-PCM RX and PCM-to-PDM TX are only supported by I2SO):**

**Diagram Components in the Image of Section Title "System Architecture":**
- CPU
- DMA
- Data and Address Bus

**Figure Caption for Figure 28.4-1 ESP32-S3 I2S System Diagram:**
"shows the structure of ESP32-S3 I2Sn module, consisting of:
- TX unit (TX control)
- RX unit (RX control)
- Input and Output Timing unit (I/O sync)
- Clock Divider (Clock Generator)
- 64 x 32-bit TX FIFO"

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)