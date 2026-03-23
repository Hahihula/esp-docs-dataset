
```markdown
Register 30.11. I2S_TX_CONF_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | I2S_SIG_LOOPBACK | I2S_TX_CHAN_MOD | (reserved) | I2S_TX_PDM_EN | I2S_TX_TDM_EN | I2S_TX_BIT_ORDER | I2S_TX_WS_IDLE_POL | I2S_TX_24_LEFT_ALIGN | (reserved) | STOP_EN | I2S_TX_PDM_BYPASS | I2S_TX_MONO_FST_VLD | I2S_TX_UPDATE | I2S_TX_BIG_ENDIAN | (reserved) | SLAVE_MOD | I2S_TX_START | I2S_TX_FIFO_RESET |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

I2S_TX_RESET Configures whether to reset TX unit.
O: No effect
1: Reset
(WT)

I2S_TX_FIFO_RESET Configures whether to reset TX FIFO.
O: No effect
1: Reset
(WT)

I2S_TX_START Configures whether to start transmitting data.
O: No effect
1: Start
(R/W/SC)

I2S_TX_SLAVE_MOD Configures whether to enable slave TX mode.
O: Disable
1: Enable
(R/W)

I2S_TX_MONO Configures whether to enable TX unit in mono mode.
O: Disable
1: Enable
(R/W)

I2S_TX_CHAN_EQUAL Configures whether to equalize left channel data and right channel data in I2S TX mono mode or TDM mode.
O: The I2S_SINGLE_DATA is invalid channel data in I2S TX mono mode or TDM mode
1: The left channel data is equal to right channel data in I2S TX mono mode or TDM mode
(R/W)

I2S_TX_BIG_ENDIAN Configures I2S TX byte endian.
O: Low address with low address value
1: Low address value to high address
(R/W)
```