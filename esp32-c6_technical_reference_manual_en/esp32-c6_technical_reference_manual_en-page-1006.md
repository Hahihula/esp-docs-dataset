

```markdown
Register 30.11. I2S_TX_CONF_REG (0x0024)

Continued from the previous page...

I2S_TX_UPDATE Configures whether to update I2S TX registers from APB clock domain to I2S TX clock domain.
O: No effect
1: Update
This bit will be cleared by hardware after update register done.
(R/W/SC)

I2S_TX_MONO_FST_VLD Configures the valid data channel in I2S TX mono mode.
O: The second channel data valid
1: The first channel data valid
(R/W)

I2S_TX_PCM_CONF Configures the I2S TX compress/decompress mode.
0 (atol): A-law decompress
1 (ltoa): A-law compress
2 (utol): μ-law decompress
3 (ltou): μ-law compress
(R/W)

I2S_TX_PCM_BYPASS Configures whether to bypass Compress/Decompress units for transmitted data.
O: No effect
1: Bypass
(R/W)

I2S_TX_STOP_EN Configures whether to stop outputting BCK signal and WS signal when TX FIFO is empty.
O: No effect
1: Stop
(R/W)

I2S_TX_LEFT_ALIGN Configures I2S TX alignment mode.
O: Right alignment mode
1: Left alignment mode
(R/W)

I2S_TX_24_FILL_EN Configures the bit number that the 24 channel bits are stored to.
0: Store 24-bit channel data to 24 bits
1: Store 24-bit channel data to 32 bits (Extra bits are filled with zeros)
(R/W)

I2S_TX_WS_IDLE_POL Configures the relationship between WS and which channel data to send.
O: WS remains low when sending left channel data and high when sending right channel data
1: WS remains high when sending left channel data and low when sending right channel data
(R/W)

Continued on the next page...
```