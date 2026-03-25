

```markdown
Register 31.11. I2S_TX_CONF_REG (0x0024)

| Bit | 31 | 30 | 29 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | I2S_SIG_LOOPBACK | I2S_TX_CHAN_MOD | I2S_TX_BCK_DV_NUM | I2S_TX_PDM_EN | I2S_TX_TDM_EN | I2S_TX_WS_BIT_ORDER | I2S_TX_WS_IDLE_POL | I2S_TX_WS_FILL_EN | I2S_TX_BK_LEFT_ALIGN | I2S_TX_BK_NO_SHIFT | I2S_TX_MSB_POM_BYPASS | I2S_TX_POM_CNF | I2S_TX_MONO_FST_VLD | I2S_TX_UPDATE | I2S_TX_BIG_ENDIAN | I2S_TX_MONO | I2S_TX_CHAN_EQUAL | I2S_TX_STOP_EN | I2S_TX_SLAVE_MOD | I2S_TX_START | I2S_TX_FIFO_RESET |
| Value | 0 | 0 | 0 | 6 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0x0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | Reset |

I2S_TX_RESET Configures whether to reset TX unit.
O: No effect
1: Reset (WT)

I2S_TX_FIFO_RESET Configures whether to reset TX FIFO.
O: No effect
1: Reset (WT)

I2S_TX_START Configures whether to start transmitting data.
O: No effect
1: Start (R/W/SC)

I2S_TX_SLAVE_MOD Configures whether to enable slave TX mode.
0: Enable master mode
1: Enable slave mode (R/W)

I2S_TX_STOP_EN Configures whether to stop outputting the BCK signal and the WS signal when TX FIFO is empty.
O: No effect
1: Stop (R/W)

I2S_TX_CHAN_EQUAL Configures whether to equalize left channel data and right channel data in I2S TX mono mode or TDM mode.
0: The I2S_SINGLE_DATA is invalid channel data in I2S TX mono mode or TDM mode
1: The left channel data is equal to right channel data in I2S TX mono mode or TDM mode (R/W)

I2S_TX_MONO Configures whether to enable TX unit in mono mode.
0: Disable
1: Enable (R/W)
```