

```markdown
Register 36.54. ISP_DMA_CNTL_REG (0x010C)

| Bit | Value |
|-----|-------|
| 31  | 0x1   |
| 20  |       |
| 19  |       |
| 8   |       |
| 7   |       |
| 2   |       |
| 1   |       |
| 0   | Reset |

ISP_DMA_EN Configures whether to trigger VDMA transfer of one frame of data.
O: Not trigger
1: Trigger
(WT)

ISP_DMA_UPDATE_REG Configures whether to update the configuration for ISP_DMA_DATA_TYPE, ISP_DMA_BURST_LEN, and ISP_DMA_INTERVAL.
O: Not update
1: Update, will be automatically cleared to 0 after the update is complete (R/W)

ISP_DMA_DATA_TYPE Configures the Image Interface data_type for the transferred data.
0x2A: RAW8
0x2B: RAW10
0x2C: RAW12
Others: Invalid
(R/W)

ISP_DMA_BURST_LEN Configures the burst length for one VDMA transfer, which needs to align with the VDMA configuration. (R/W)

ISP_DMA_INTERVAL Configures the interval of VDMA requests. 12'b1: 1 clock cycle, 12'b11: 2 clock cycles, etc. (R/W)
```