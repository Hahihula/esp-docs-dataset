

```markdown
Register 39.76. H264_DMA_OUT_CONF0_CH3_REG (0x0300)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | H264_DMA_OUT_ARB_WEIGHT_OPT_DS_CH3         | (reserved)                                                                  |
| 29  |                                             |                                                                             |
| 28  |                                             |                                                                             |
| 27  |                                             |                                                                             |
| 26  |                                             |                                                                             |
| 25  |                                             |                                                                             |
| 13  | H264_DMA_OUT_PAGE_BOUND_EN_CH3             | (reserved)                                                                  |
| 12  |                                             |                                                                             |
| 11  |                                             |                                                                             |
| 10  |                                             |                                                                             |
| 9   |                                             |                                                                             |
| 8   |                                             |                                                                             |
| 7   | H264_DMA_OUT_MEM_BURST_LENGTH_CH3          | (reserved)                                                                  |
| 6   |                                             |                                                                             |
| 5   |                                             |                                                                             |
| 4   |                                             |                                                                             |
| 3   |                                             |                                                                             |
| 2   |                                             |                                                                             |
| 1   | H264_DMA_OUT_CHECK_OWNER_CH3               | (reserved)                                                                  |
| 0   | Reset                                      | 0x0                                                                          |

H264_DMA_OUT_AUTO_WRBACK_CH3 Configures whether to enable automatic outlink-writeback when all the data pointed by outlink descriptor has been received.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_EOF_MODE_CH3 Configures EOF flag generation mode for TX channel 3.
- O: EOF flag is generated when last data has been pushed into FIFO in DMA
- 1: EOF flag is generated when last data has been popped from FIFO in DMA
(R/W)

H264_DMA_OUTDSCR_BURST_EN_CH3 Configures whether to enable INCR burst transfer for TX channel 3 to read descriptors.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_ECC_AES_EN_CH3 Configures whether DMA can access external memory space for ECC and AES via TX channel 3.
- O: Not access
- 1: Access ECC/AES area. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_OUT_CHECK_OWNER_CH3 Configures whether to enable owner bit check for TX channel 3.
- O: Disable
- 1: Enable
(R/W)
```