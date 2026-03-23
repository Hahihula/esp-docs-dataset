

```markdown
Register 30.12. I2S_TX_CONF1_REG (0x002C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2S_TX_BCK_NO_DLY                                                           |
| 29  | I2S_TX_MSB_SHIFT                                                            |
| 28  | I2S_TX_TDM_CHAN_BITS                                                       |
| 24  | I2S_TX_HALF_SAMPLE_BITS                                                    |
| 18  | I2S_TX_BITS_MOD                                                             |
| 17  | I2S_TX_BCK_DIV_NUM                                                          |
| 6   | I2S_TX_TDM_WS_WIDTH                                                         |

I2S_TX_TDM_WS_WIDTH Configures the width of tx_ws_out (WS default level) in TDM mode. The width of tx_ws_out (WS default level) in TDM mode = (I2S_TX_TDM_WS_WIDTH[6:0] + 1) x T_BCK. (R/W)

I2S_TX_BCK_DIV_NUM Configures the divider of BCK in TX mode. Note this divider must not be configured to 1. (R/W)

I2S_TX_BITS_MOD Configures the valid data bit length of I2S TX channel.
7: All the valid channel data is in 8-bit mode
15: All the valid channel data is in 16-bit mode
23: All the valid channel data is in 24-bit mode
31: All the valid channel data is in 32-bit mode
Other values are invalid.
(R/W)

I2S_TX_HALF_SAMPLE_BITS Configures I2S TX sample bits. BCK cycles in one WS period = I2S_TX_HALF_SAMPLE_BITS x 2. (R/W)

I2S_TX_TDM_CHAN_BITS Configures TX bit number for each channel in TDM mode. Bit number expected = I2S_TX_TDM_CHAN_BITS + 1. (R/W)

I2S_TX_MSB_SHIFT Configures the timing between WS signal and the MSB of data.
0: Align at rising edge
1: WS signal changes one BCK clock earlier
(R/W)

I2S_TX_BCK_NO_DLY Configures whether BCK is delayed to generate rising/falling edge in master mode.
0: Delayed
1: Not delayed
(R/W)
```