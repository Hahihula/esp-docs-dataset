

```markdown
Register 4.66. AHB_DMA_AHBINF_RESP_ERR_STATUS1_REG (0x040C)
```

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0xO | 0xF | 0xO | Reset |

**AHB_DMA_AHBINF_RESP_ERR_CH_ID** Represents the channel ID of the transfer that triggers the AHB bus error response.

Bits[0:1]: Channel number. Value range: 0 ~2

Bit[2]: Channel direction. O: RX
1: TX
(RO)

**AHB_DMA_AHBINF_RESP_ERR_ID** Represents the ID of the transfer that triggers the AHB bus error response.

1: Transfer between GP-SPI and memory
2: Transfer between UHCI and memory
3: Transfer between I2S and memory
6: Transfer between AES and memory
7: Transfer between SHA and memory
8: Transfer between ADC and memory
9: Transfer between PARIO and memory
11: Memory-to-memory transfer on channel 1
12: Memory-to-memory transfer on channel 2

Other values are invalid
(RO)

**AHB_DMA_AHBINF_RESP_ERR_WR** Represents the type of the transfer that triggered the AHB bus error response received by the AHB DMA.

O: Read
1: Write
(RO)
```