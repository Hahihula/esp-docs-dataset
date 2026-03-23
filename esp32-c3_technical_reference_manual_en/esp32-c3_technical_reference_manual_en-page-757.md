

```markdown
Register 29.12. I2S_TX_CONF_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | I2S_SIG_LOOPBACK | I2S_TX_CHAN_MOD | (reserved) | I2S_TX_PDM_EN | I2S_TX_TDM_EN | I2S_TX_WS_IDLE_POL | I2S_TX_LEFT_ALIGN | I2S_TX_BIT_ORDER | I2S_TX_WIDEN | STOP_EN | I2S_TX_PCM_BYPASS | I2S_TX_FST_VLD | I2S_TX_BIG_ENDIAN | I2S_TX_MONO | I2S_TX_EQUAL | (reserved) | I2S_TX_START | I2S_TX_RESET |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

I2S_TX_RESET    Set this bit to reset TX unit. (WT)
I2S_TX_FIFO_RESET   Set this bit to reset TX FIFO. (WT)
I2S_TX_START     Set this bit to start transmitting data. (R/W)
I2S_TX_SLAVE_MOD   Set this bit to enable slave TX mode. (R/W)
I2S_TX_MONO      Set this bit to enable TX unit in mono mode. (R/W)
I2S_TX_CHAN_EQUAL 1: The left channel data is equal to right channel data in I2S TX mono mode or TDM mode. 0: The invalid channel data is I2S_SINGLE_DATA in I2S TX mono mode or TDM mode. (R/W)
I2S_TX_BIG_ENDIAN   I2S TX byte endian. 1: low address data is saved to high address. 0: low address data is saved to low address. (R/W)
I2S_TX_UPDATE     Set 1 to update I2S TX registers from APB clock domain to I2S TX clock domain. This bit will be cleared by hardware after register update is done. (R/W/SC)
I2S_TX_MONO_FST_VLD 1: The first channel data is valid in I2S TX mono mode. 0: The second channel data is valid in I2S TX mono mode. (R/W)
I2S_TX_PCM_CONF   I2S TX compress/decompress configuration bits. 0 (atol): A-law decompress, 1 (ltoa): A-law compress, 2 (utol): μ-law decompress, 3 (ltou): μ-law compress. (R/W)
I2S_TX_PCM_BYPASS Set this bit to bypass Compress/Decompress module for transmitted data. (R/W)
I2S_TX_STOP_EN    Set this bit to stop outputting BCK signal and WS signal when TX FIFO is empty. (R/W)
I2S_TX_LEFT_ALIGN 1: I2S TX left alignment mode. 0: I2S TX right alignment mode. (R/W)
I2S_TX_24_FILL_EN 1: Set 32 bits in 24-bit channel data mode. (Extra bits are filled with zeros). 0: Sent 24 bits in 24-bit channel data mode. (R/W)
I2S_TX_WS_IDLE_POL 0: WS remains low when sending left channel data, and remains high when sending right channel data. 1: WS remains high when sending left channel data, and remains low when sending right channel data. (R/W)
I2S_TX_BIT_ORDER Configures whether to reverse the bit order of valid data to be sent by the I2S TX. 0: Not reverse. 1: Reverse. (R/W)
I2S_TX_TDM_EN     1: Enable I2S TDM TX mode. 0: Disable I2S TDM TX mode. (R/W)
```