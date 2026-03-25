

```markdown
Register 35.5. I2S_RX_CONF_REG (0x0020)

Continued from the previous page...

I2S_RX_UPDATE Configures whether to update I2S RX registers from APB clock domain to I2S RX clock domain.
O: No effect
1: Update
This bit will be cleared by hardware after the register update is done.
(R/W/SC)

I2S_RX_MONO_FST_VLD Configures the valid data channel in I2S RX mono mode.
O: The second channel data valid
1: The first channel data valid
(R/W)

I2S_RX_PCM_CONF Configures I2S RX compress/decompress mode.
O (atol): A-law decompress
1 (Itoa): A-law compress
2 (utol): μ-law decompress
3 (ltou): μ-law compress
(R/W)

I2S_RX_PCM_BYPASS Configures whether to bypass the Compress/Decompress units for received data.
O: No effect
1: Bypass
(R/W)

I2S_RX_MSB_SHIFT Configures the timing between the WS signal and the MSB of data.
O: Align at the rising edge
1: The WS signal changes one BCK clock earlier
(R/W)

I2S_RX_DONE_MODE Configures when to trigger the I2S_RX_DONE_INT interrupt.
O: When RX FIFO is full
1: When IN_SUC_EOF is 1
(R/W)

I2S_RX_LEFT_ALIGN Configures I2S RX alignment mode.
O: Right alignment mode
1: Left alignment mode
(R/W)

I2S_RX_24_FILL_EN Configures the bit number that the 24-bit channel data is stored to.
O: Store 24-bit channel data to 24 bits
1: Store 24-bit channel data to 32 bits (Extra bits are filled with zeros)
(R/W)

Continued on the next page...
```