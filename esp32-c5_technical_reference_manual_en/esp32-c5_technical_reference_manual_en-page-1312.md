

```markdown
Register 35.9. I2S_TX_CONF_REG (0x0024)

Continued from the previous page...

I2S_TX_24_FILL_EN Configures the bit number that the 24 channel bits are stored to.
O: Store 24-bit channel data to 24 bits
1: Store 24-bit channel data to 32 bits (Extra bits are filled with zeros)
(R/W)

I2S_TX_WS_IDLE_POL Configures the relationship between WS and which channel data to transmit.
O: WS remains low when transmitting left channel data and high when transmitting right channel data
1: WS remains high when transmitting left channel data and low when transmitting right channel data
(R/W)

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

I2S_TX_BCK_DIV_NUM Configures the divider of BCK in TX mode. Note this divider must not be configured to 1. (R/W)

I2S_TX_CHAN_MOD Configures I2S TX channel mode. For more information, see Table 35.9-4.
(R/W)

I2S_SIG_LOOPBACK Configures whether to enable TX unit and RX unit sharing the same WS and BCK signals.
O: Disable
1: Enable
(R/W)
```