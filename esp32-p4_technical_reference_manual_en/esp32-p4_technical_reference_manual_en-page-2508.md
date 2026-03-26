

```markdown
Register 47.2. LP_I2S_RX_CONF_REG (0x0020)
```

Continued from the previous page...

LP_I2S_RX_WS_IDLE_POL Configures the relationship between WS level and which channel data to receive.
- O: WS remains low when receiving left channel data and high when receiving right channel data
- 1: WS remains high when receiving left channel data and low when receiving right channel data (R/W)

LP_I2S_RX_BIT_ORDER Configures whether to reverse the bit order of the LP I2S RX data to be received.
- O: Not reverse
- 1: Reverse (R/W)

LP_I2S_RX_TDM_EN Configures whether to enable LP I2S TDM RX mode.
- O: Disable
- 1: Enable (R/W)

LP_I2S_RX_PDM_EN Configures whether to enable LP I2S PDM RX mode.
- O: Disable
- 1: Enable (R/W)
```