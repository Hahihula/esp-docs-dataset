

```markdown
Register 30.5. I2S_RX_CONF_REG (0x0020)

Continued from the previous page...

I2S_RX_MONO_FST_VLD Configures the valid data channel in I2S RX mono mode.
    0: The second channel data valid
    1: The first channel data valid
    (R/W)

I2S_RX_PCM_CONF Configures I2S RX compress/decompress mode.
    0 (atol): A-law decompress
    1 (ltoa): A-law compress
    2 (utol): μ-law decompress
    3 (ltou): μ-law compress
    (R/W)

I2S_RX_PCM_BYPASS Configures whether to bypass the Compress/Decompress units for received data.
    0: No effect
    1: Bypass
    (R/W)

I2S_RX_STOP_MODE Configures I2S RX stop mode.
    0: I2S RX only stops when REG_TXRX_START is cleared
    1: I2S RX stops when REG_TXRX_START is 0 or in_suc_eof is 1
    2: I2S RX stops when REG_TXRX_START is 0 or RX FIFO is full
    (R/W)

I2S_RX_LEFT_ALIGN Configures I2S RX alignment mode.
    0: Right alignment mode
    1: Left alignment mode
    (R/W)

I2S_RX_24_FILL_EN Configures the bit number that the 24-bit channel data is stored to.
    0: Store 24-bit channel data to 24 bits
    1: Store 24-bit channel data to 32 bits (Extra bits are filled with zeros)
    (R/W)

I2S_RX_WS_IDLE_POL Configures the relationship between WS level and which channel data to receive.
    0: WS remains low when receiving left channel data and high when receiving right channel data
    1: WS remains high when receiving left channel data and low when receiving right channel data
    (R/W)

Continued on the next page...
```