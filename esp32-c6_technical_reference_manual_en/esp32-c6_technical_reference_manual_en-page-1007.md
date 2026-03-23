

```markdown
Chapter 30 I2S Controller (I2S) GoBack

Register 30.11. I2S_TX_CONF_REG (0x0024)

Continued from the previous page...

I2S_TX_BIT_ORDER Configures whether to reverse the bit order of valid data to be sent by the I2S TX.
O: Not reverse
1: Reverse
(R/W)

I2S_TX_TDM_EN Configures whether to enable I2S TDM TX mode.
O: Disable
1: Enable
(R/W)

I2S_TX_PDM_EN Configures whether to enable I2S PDM TX mode.
O: Disable
1: Enable
(R/W)

I2S_TX_CHAN_MOD Configures I2S TX channel mode. For more information, see Table 30.9-5.
(R/W)

I2S_SIG_LOOPBACK Configures whether to enable TX unit and RX unit sharing the same WS and BCK signals.
O: Disable
1: Enable
(R/W)
```