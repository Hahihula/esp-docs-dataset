

```markdown
Register 35.14. I2S_RX_TIMING_REG (0x0058)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0x0| 0  | 0  | 0x0| 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | I2S_RX_SD_IN_DM | (reserved) | I2S_RX_SD1_IN_DM | (reserved) | I2S_RX_SD2_IN_DM | (reserved) | I2S_RX_SD3_IN_DM | (reserved) | I2S_RX_WS_OUT_DM | (reserved) | I2S_RX_BCK_OUT_DM | (reserved) | I2S_RX_WS_IN_DM | (reserved) | I2S_RX_BCK_IN_DM |
```

I2S_RX_SD_IN_DM Configures the delay mode of I2S RX SD input signal.
0: Bypass
1: Delay by rising edge
2: Delay by falling edge
3: Invalid
(R/W)

I2S_RX_SD1_IN_DM Configures the delay mode of I2S RX SD1 input signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_SD2_IN_DM Configures the delay mode of I2S RX SD2 input signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_SD3_IN_DM Configures the delay mode of I2S RX SD3 input signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_WS_OUT_DM Configures the delay mode of I2S RX WS output signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_BCK_OUT_DM Configures the delay mode of I2S RX BCK output signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_WS_IN_DM Configures the delay mode of I2S RX WS input signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)

I2S_RX_BCK_IN_DM Configures the delay mode of I2S RX BCK input signal. For detailed configuration values, please refer to I2S_RX_SD_IN_DM. (R/W)
```