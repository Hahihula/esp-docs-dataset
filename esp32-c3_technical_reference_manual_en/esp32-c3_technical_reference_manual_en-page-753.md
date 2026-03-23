

```markdown
Register 29.5. I2S_RX_CONF_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    | (reserved) | I2S_RX_PDM_EN | I2S_RX_TDM_EN | I2S_RX_BIT_ORDER | I2S_RX_WS_IDLE_POL | I2S_RX_WS_FILL_EN | I2S_RX_LEFT_ALIGN | I2S_RX_STOP_MODE | I2S_RX_PCM_BYPASS | I2S_RX_PCM_CONF | I2S_RX_UPDATE | I2S_RX_MONO_FST_VLD | I2S_RX_BIG_ENDIAN | I2S_RX_MONO | (reserved) | I2S_RX_PCM_CONF | I2S_RX_PDM_EN |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 0x1 | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | Reset |

I2S_RX_RESET Set this bit to reset RX unit. (WT)

I2S_RX_FIFO_RESET Set this bit to reset RX FIFO. (WT)

I2S_RX_START Set this bit to start receiving data. (R/W)

I2S_RX_SLAVE_MOD Set this bit to enable slave RX mode. (R/W)

I2S_RX_MONO Set this bit to enable RX unit in mono mode. (R/W)

I2S_RX_BIG_ENDIAN I2S RX byte endian. 1: low address data is saved to high address. 0: low address data is saved to low address. (R/W)

I2S_RX_UPDATE Set 1 to update I2S RX registers from APB clock domain to I2S RX clock domain. This bit will be cleared by hardware after register update is done. (R/W/SC)

I2S_RX_MONO_FST_VLD 1: The first channel data is valid in I2S RX mono mode. 0: The second channel data is valid in I2S RX mono mode. (R/W)

I2S_RX_PCM_CONF I2S RX compress/decompress configuration bit. 0 (atol): A-law decompress, 1 (Itoa): A-law compress, 2 (utol): μ-law decompress, 3 (ltou): μ-law compress. (R/W)

I2S_RX_PCM_BYPASS Set this bit to bypass Compress/Decompress module for received data. (R/W)

I2S_RX_STOP_MODE 0: I2S RX stops only when I2S_RX_START is cleared. 1: I2S RX stops when I2S_RX_START is 0 or in_suc_eof is 1. 2: I2S RX stops when I2S_RX_START is 0 or RX FIFO is full. (R/W)

I2S_RX_LEFT_ALIGN 1: I2S RX left alignment mode. 0: I2S RX right alignment mode. (R/W)

I2S_RX_24_FILL_EN 1: store 24-bit channel data to 32 bits (Extra bits are filled with zeros). 0: store 24-bit channel data to 24 bits. (R/W)

I2S_RX_WS_IDLE_POL 0: WS remains low when receiving left channel data, and remains high when receiving right channel data. 1: WS remains high when receiving left channel data, and remains low when receiving right channel data. (R/W)

I2S_RX_BIT_ORDER Configures whether to reverse the bit order of the I2S RX data to be received. 0: Not reverse. 1: Reverse. (R/W)

I2S_RX_TDM_EN 1: Enable I2S TDM RX mode. 0: Disable I2S TDM RX mode. (R/W)

I2S_RX_PDM_EN 1: Enable I2S PDM RX mode. 0: Disable I2S PDM RX mode. (R/W)
```