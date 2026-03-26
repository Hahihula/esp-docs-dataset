

```markdown
Register 47.2. LP_I2S_RX_CONF_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 1  | 0  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

LP_I2S_RX_RESET Configures whether to reset RX.
- 0: No effect
- 1: Reset (WT)

LP_I2S_RX_FIFO_RESET Configures whether to reset RX FIFO.
- 0: No effect
- 1: Reset (WT)

LP_I2S_RX_START Configures whether to start receiving data.
- 0: No effect
- 1: Start (R/W)
```