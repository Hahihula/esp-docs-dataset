

```markdown
Register 29.12. I2S_TX_CONF_REG (0x0024)

Continued from the previous page...

I2S_TX_PDM_EN    1: Enable I2S PDM TX mode. 0: Disable I2S PDM TX mode. (R/W)

I2S_TX_CHAN_MOD   I2S TX channel configuration bits. For more information, see Table 29.9-4.
(R/W)

I2S_SIG_LOOPBACK  Enable signal loop back mode with TX unit and RX unit sharing the same WS
and BCK signals. (R/W)


Register 29.13. I2S_TX_CONF1_REG (0x002C)
```

```markdown
| 31 | 30 | 29 | 28 | 24 | 23 | 18 | 17 | 13 | 12 | 7 | 6 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
|   0 |   1 |     | Oxf | Oxf | Oxf | Oxf |    |    |    | Ox0 | Reset |
```

```markdown
I2S_TX_TDM_WS_WIDTH The width of tx_ws_out (WS default level) in TDM mode is
(I2S_TX_TDM_WS_WIDTH + 1) * T_BCK. (R/W)

I2S_TX_BCK_DIV_NUM Configure the divider of BCK in TX mode. Note this divider must not be
configured to 1. (R/W)

I2S_TX_BITS_MOD Set the bits to configure the valid data bit length of I2S TX channel.
7: all the valid channel data is in 8-bit mode. 15: all the valid channel data is in 16-bit mode.
23: all the valid channel data is in 24-bit mode. 31: all the valid channel data is in 32-bit mode.
(R/W)

I2S_TX_HALF_SAMPLE_BITS I2S TX half sample bits. This value x 2 is equal to the BCK cycles in
one WS period. (R/W)

I2S_TX_TDM_CHAN_BITS Configure TX bit number for each channel in TDM mode. Bit number
expected = this value + 1. (R/W)

I2S_TX_MSB_SHIFT Control the timing between WS signal and the MSB of data.
1: WS signal changes one BCK clock earlier. 0: Align at rising edge. (R/W)

I2S_TX_BCK_NO_DLY 1: BCK is not delayed to generate rising/falling edge in master mode.
0: BCK is delayed to generate rising/falling edge in master mode. (R/W)
```