

```markdown
## Register 39.117. H264_DMA_IN_ARB_CH5_REG (0x0A40)

| Bit | Description |
|-----|-------------|
| 31-8 | (reserved) |
| 7:6 | H264_DMA_INTER_IN_ARB_PRIORITY_CH5<br>Configures the priority of internal memory access for RX channel 5. (R/W) |
| 5:4 | (reserved) |
| 3:0 | H264_DMA_IN_ARB_TOKEN_NUM_CH5<br>Configures the maximum token count for the arbiter configuration. (R/W) |

## Register 39.118. H264_DMA_RST_CONF_REG (0x0B08)

| Bit | Description |
|-----|-------------|
| 31-7 | (reserved) |
| 6:5 | H264_DMA_CLK_EN<br>Configures DMA clock gating.<br>0: Enable the clock only when the application writes registers<br>1: Always enable the clock for registers (R/W) |
| 4:3 | H264_DMA_INTER_AXIM_RD_RST<br>Write 1 and then 0 to reset the inter AXI read FSM. (R/W) |
| 2:1 | H264_DMA_INTER_AXIM_WR_RST<br>Write 1 and then 0 to reset the inter AXI write FSM. (R/W) |
| 0   | H264_DMA_EXTER_AXIM_RD_RST<br>Write 1 and then 0 to reset the ext AXI read FSM. (R/W) |

```