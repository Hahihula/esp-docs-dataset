**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Header:**
22.6.2 DMA Interrupts

**Body Text:**
- I2S_OUT_TOTAL_EOF_INT: Triggered when all transmitting linked lists are used up.
- I2S_IN_DSCR_EMPTY_INT: Triggered when there are no valid receiving linked lists left.
- I2S_OUT_DSCR_ERR_INT: Triggered when invalid txlink descriptors are encountered.
- I2S_IN_DSCR_ERR_INT: Triggered when invalid rxlink descriptors are encountered.
- I2S_OUT_EOF_INT: Triggered when txlink has finished sending a packet.
- I2S_OUT_DONE_INT: Triggered when all transmitted and buffered data have been read.
- I2S_IN_SUC_EOF_INT: Triggered when all data have been received.
- I2S_IN_DONE_INT: Triggered when the current rxlink descriptor is handled.

**Subsection Header:**
22.7 Register Summary

**Body Text with Table Description:**
The addresses in this section are relative to the I2S base address provided in Table 3.3-6 in Chapter 3 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | IS20 | Is21 | Acc |
|------|-------------|-----|-----|-----|
| I2S_FIFOregisters | Writes the data sent by I2S into FIFO | 0x3FF4F000 | 0x3FF6D000 | WO |
| I2S_FIFO_WR_REG |  |  |  |  |
| I2S_FIFO_RD_REG | Stores the data that I2S receives from FIFO | 0x3FF4F004 | 0x3FF6D004 | RO |
| **Configuration registers** |  |  |  |  |
| I2S_CONF_REG | Configuration and start/stop bits | 0x3FF4F008 | 0x3FF6D008 | R/W |
| I2S_CONF1_REG | PCM configuration register | 0x3FF4F0A0 | 0x3FF6D0A0 | R/W |
| I2S_CONF2_REG | ADC/LCD/camera configuration register | 0x3FF4F0A8 | 0x3FF6D0A8 | R/W |
| I2S_TIMING_REG | Signal delay and timing parameters | 0x3FF4F01C | 0x3FF6D01C | R/W |
| I2S_FIFO_CONF_REG | FIFO configuration | 0x3FF4F020 | 0x3FF6D020 | R/W |
| I2S_CONF_SINGLE_DATA_REG | Static channel output value | 0x3FF4F028 | 0x3FF6D028 | R/W |
| I2S_CONF_CHAN_REG | Channel configuration | 0x3FF4F02C | 0x3FF6D02C | RO |
| I2S_LCHUNG_CONF_REG | Timeout detection configuration | 0x3FF4F074 | 0x3FF6D074 | R/W |
| I2S_CLKM_CONF_REG | Bitclock configuration | 0x3FF4F0AC | 0x3FF6D0AC | RO |
| I2S_SAMPLE_RATE_CONF_REG | Sample rate configuration | 0x3FF4F0B0 | 0x3FF6D0BO | R/W |
| **DMA registers** |  |  |  |  |
| I2S_LC_CONF_REG | DMA configuration register | 0x3FF4F060 | 0x3FF6D060 | R/W |
| I2S_RXEOF_NUM_REG | Receive data count | 0x3FF4F024 | 0x3FF6D024 | RO |

**Footer:**
Espressif Systems
Page number and document version:
430 ESP32 TRM (Version 5.6)