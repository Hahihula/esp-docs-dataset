

```markdown
Register 46.10. I2S_TX_CONF_REG (0x0024)

Continued from the previous page...

I2S_TX_BIG_ENDIAN Configures I2S TX byte endian.
- 0: Low address with low address value
- 1: Low address value to high address
(R/W)

I2S_TX_UPDATE Configures whether to update I2S TX registers from APB clock domain to I2S TX clock domain.
- 0: No effect
- 1: Update
This bit will be cleared by hardware after update register done.
(R/W/SC)

I2S_TX_MONO_FST_VLD Configures the valid data channel in I2S TX mono mode.
- 0: The second channel data valid
- 1: The first channel data valid
(R/W)

I2S_TX_PCM_CONF Configures the I2S TX compress/decompress mode.
- 0 (atol): A-law decompress
- 1 (Itoa): A-law compress
- 2 (utol): μ-law decompress
- 3 (Itou): μ-law compress
(R/W)

I2S_TX_PCM_BYPASS Configures whether to bypass Compress/Decompress units for transmitted data.
- 0: No effect
- 1: Bypass
(R/W)

I2S_TX_MSB_SHIFT Configures the timing between the WS signal and the MSB of data.
- 0: Align at the rising edge
- 1: WS signal changes one BCK clock earlier
(R/W)

I2S_TX_BCK_NO_DLY Configures the source of the BCK rising and falling edges in master mode.
- 0: Rising and falling edges are constructed based on the BCK input from I2SnO_BCK_in
- 1: Rising and falling edges are constructed by dividing the clock of I2Sn TX
(R/W)

I2S_TX_LEFT_ALIGN Configures I2S TX alignment mode.
- 0: Right alignment mode
- 1: Left alignment mode
(R/W)

Continued on the next page...
```