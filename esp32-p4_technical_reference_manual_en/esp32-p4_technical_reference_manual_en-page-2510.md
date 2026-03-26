

```markdown
## Register 47.4. LP_I2S_RX_TDM_CTRL_REG (0x0050)

LP_I2S_RX_TDM_PDM_CHAN0_EN Configures whether to enable the valid data input of LP I2S RX TDM or PDM channel 0.
O: Disable. Channel 0 only inputs O
1: Enable
(R/W)

LP_I2S_RX_TDM_PDM_CHAN1_EN Configures whether to enable the valid data input of LP I2S RX TDM or PDM channel 1.
O: Disable. Channel 1 only inputs O
1: Enable
(R/W)

LP_I2S_RX_TDM_TOT_CHAN_NUM Configures the total channel number of LP I2S RX TDM mode.
Total channel number in use = LP_I2S_RX_TDM_TOT_CHAN_NUM + 1. (R/W)
```

```markdown
## Register 47.5. LP_I2S_RXEOF_NUM_REG (0x0064)

LP_I2S_RX_EOF_NUM Configures the bit length of RX data.
Bit length of RX data = (LP_I2S_RX_BITS_MOD[4:0] + 1) x (LP_I2S_RX_EOF_NUM[11:0] + 1).
Valid when LP_I2S_RX_STOP_MODE is set to 1. (R/W)
```