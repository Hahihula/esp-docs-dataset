

```markdown
Register 31.5. I2S_RX_CONF_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | I2S_RX_BCK_DIV_NUM | I2S_RX_PDM_EN | I2S_RX_IDM_EN | I2S_RX_WS_BIT_ORDER | I2S_RX_IDLE_POL | I2S_RX_FILL_EN | (reserved) | I2S_RX_LEFT_ALIGN | MSB_SHIFT | PCM_PCM_CONF | RX_UPDATE | I2S_RX_FST_VLD | I2S_RX_MONO | I2S_RX_BIG_ENDIAN | I2S_RX_STOP_MODE | I2S_RX_SLAVE_MOD | I2S_RX_START | I2S_RX_FIFO_RESET |

I2S_RX_RESET Configures whether to reset RX unit.
0: No effect
1: Reset
(WT)

I2S_RX_FIFO_RESET Configures whether to reset RX FIFO.
0: No effect
1: Reset
(WT)

I2S_RX_START Configures whether to start receiving data.
0: No effect
1: Start
(R/W/SC)

I2S_RX_SLAVE_MOD Configures whether to enable slave RX mode.
0: Enable master mode
1: Enable slave mode
(R/W)

I2S_RX_STOP_MODE Configures when I2S RX stop data reception.
0: Only stops when I2S_RX_START is cleared
1: Stops when I2S_RX_START is cleared or the number of received bytes is greater than the value configured in I2S_RX_EOF_NUM_REG
2: Stops when I2S_RX_START is cleared or GDMA RX FIFO is full
(R/W)

I2S_RX_MONO Configures whether to enable RX unit in mono mode.
0: Disable
1: Enable
(R/W)

I2S_RX_BIG_ENDIAN Configures I2S RX byte endian.
0: Low address data is saved to low address
1: Low address data is saved to high address
(R/W)
```