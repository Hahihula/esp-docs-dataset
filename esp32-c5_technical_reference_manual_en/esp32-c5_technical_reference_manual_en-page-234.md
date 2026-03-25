

```markdown
Register 5.50. AHB_DMA_AHBINF_RESP_ERR_STATUS1_REG (0x040C)
```

| Bit | Field Name | Description |
|-----|------------|-------------|
| 31  |            |             |
|     |            | (reserved)  |
| 7   |            | AHB_DMA_AHBINF_RESP_ERR_CH_ID |
| 5   |            | AHB_DMA_AHBINF_RESP_ERR_ID |
| 4   |            | AHB_DMA_AHBINF_RESP_ERR_WR |
| 0   | Reset      | 0x0         |

**AHB_DMA_AHBINF_RESP_ERR_CH_ID** Represents the channel ID of the transfer that triggers the AHB bus error response.
- Bits[0:1]: Channel number. Value range: 0 ~ 2
- Bit[2]: Channel direction. O: RX<br>1: TX (RO)

**AHB_DMA_AHBINF_RESP_ERR_ID** Represents the ID of the transfer that triggers the AHB bus error response.
1: Transfer between GP-SPI and memory
2: Transfer between UHCI and memory
3: Transfer between I2S and memory
6: Transfer between AES and memory
7: Transfer between SHA and memory
8: Transfer between ADC and memory
9: Transfer between PARIIO and memory
10: Memory-to-memory transfer on channel 0
11: Memory-to-memory transfer on channel 1
12: Memory-to-memory transfer on channel 2
Other values are invalid (RO)

**AHB_DMA_AHBINF_RESP_ERR_WR** Represents the type of the transfer that triggered the AHB bus error response received by the GDMA.
0: Read<br>1: Write (RO)
```