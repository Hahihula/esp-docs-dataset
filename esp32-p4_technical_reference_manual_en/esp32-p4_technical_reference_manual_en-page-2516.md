

```markdown
Register 47.11. LP_I2S_RX_TIMING_REG (0x0058)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | LP_I2S_RX_BCK_IN_DM | (reserved) | LP_I2S_RX_WS_IN_DM | (reserved) | LP_I2S_RX_OUT_DM | (reserved) | LP_I2S_RX_WS_OUT_DM | (reserved) | LP_I2S_RX_SD_IN_DM |
| Value | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 |

LP_I2S_RX_SD_IN_DM Configures the delay mode of LP I2S RX SD input signal.
O: Bypass
1: Delay by positive edge
2: Delay by negative edge
3: Invalid
(R/W)

LP_I2S_RX_WS_OUT_DM Configures the delay mode of LP I2S RX WS output signal. For detailed configuration values, please refer to LP_I2S_RX_SD_IN_DM. (R/W)

LP_I2S_RX_BCK_OUT_DM Configures the delay mode of LP I2S RX BCK output signal. For detailed configuration values, please refer to LP_I2S_RX_SD_IN_DM. (R/W)

LP_I2S_RX_WS_IN_DM Configures the delay mode of LP I2S RX WS input signal. For detailed configuration values, please refer to LP_I2S_RX_SD_IN_DM.(R/W)

LP_I2S_RX_BCK_IN_DM Configures the delay mode of LP I2S RX BCK input signal. For detailed configuration values, please refer to LP_I2S_RX_SD_IN_DM. (R/W)
```