

```markdown
Register 39.86. H264_DMA_IN_CONFO_CHO_REG (0x0500)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | (reserved)                                                                  |
| 30  |                                            | (reserved)                                                                  |
| 29  | H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CHO         |                                                                             |
| 28  | H264_DMA_IN_CMD_DISABLE_CHO                |                                                                             |
| 27  | H264_DMA_IN_RST_CHO                        |                                                                             |
| 26  |                                            | (reserved)                                                                  |
| 25  |                                            | (reserved)                                                                  |
| 24  |                                            | (reserved)                                                                  |
| 23  |                                            | (reserved)                                                                  |
| 13  | H264_DMA_IN_PAGE_BOUND_EN_CHO              |                                                                             |
| 12  |                                            | (reserved)                                                                  |
| 11  | H264_DMA_IN_MEM_BURST_LENGTH_CHO           |                                                                             |
| 10  | H264_DMA_IN_CHECK_OWNER_CHO                |                                                                             |
| 9   | H264_DMA_IN_ECC_AES_EN_CHO                 |                                                                             |
| 8   |                                            | (reserved)                                                                  |
| 7   |                                            | (reserved)                                                                  |
| 6   |                                            | (reserved)                                                                  |
| 5   |                                            | (reserved)                                                                  |
| 4   |                                            | (reserved)                                                                  |
| 3   |                                            | (reserved)                                                                  |
| 2   |                                            | (reserved)                                                                  |
| 1   |                                            | (reserved)                                                                  |
| 0   |                                            | Reset                                                                        |

H264_DMA_INDSCR_BURST_EN_CHO Configures whether to enable INCR burst transfer for RX channel 0 to read descriptors.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ECC_AES_EN_CHO Configures whether DMA can access external memory space for ECC and AES via RX channel 0.
O: Not access
1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_IN_CHECK_OWNER_CHO Configures whether to enable owner bit check for RX channel 0.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_MEM_BURST_LENGTH_CHO Configures the burst length for RX channel 0.
O: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
5 ~ 7: Invalid
(R/W)

H264_DMA_IN_PAGE_BOUND_EN_CHO Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
O: AXI read data can cross the address boundary
1: AXI read data doesn't cross the address boundary
(R/W)

H264_DMA_IN_RST_CHO Write 1 then write 0 to reset RX channel 0. (R/W)
```
Continued on the next page...
```