

```markdown
Register 39.92. H264_DMA_IN_CONFO_CH1_REG (0x0600)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH1        | Configures whether to enable INCR burst transfer for RX channel 1 to read descriptors. |
|     |                                            | O: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 29  | H264_DMA_IN_CMD_DISABLE_CH1               | Configures whether DMA can access external memory space for ECC and AES via RX channel 1. |
|     |                                            | O: Not access                                                                |
|     |                                            | 1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned. (R/W) |
| 28  | H264_DMA_IN_RST_CH1                       | Configures whether to enable owner bit check for RX channel 1.               |
|     |                                            | O: Disable                                                                   |
|     |                                            | 1: Enable                                                                    |
|     | (R/W)                                     |                                                                             |
| 27  | H264_DMA_IN_PAGE_BOUND_EN_CH1             | Configures the burst length for RX channel 1.                               |
|     |                                            | O: 8 bytes                                                                   |
|     |                                            | 1: 16 bytes                                                                  |
|     |                                            | 2: 32 bytes                                                                  |
|     |                                            | 3: 64 bytes                                                                  |
|     |                                            | 4: 128 bytes                                                                 |
|     |                                            | 5 ~ 7: Invalid                                                               |
|     | (R/W)                                     |                                                                             |
| 26  | H264_DMA_IN_MEM_BURST_LENGTH_CH1          | Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length. |
|     |                                            | O: AXI read data can cross the address boundary                              |
|     |                                            | 1: AXI read data doesn't cross the address boundary                          |
|     | (R/W)                                     |                                                                             |
| 25  | H264_DMA_IN_CHECK_OWNER_CH1               | Write 1 then write 0 to reset RX channel 1. (R/W)                            |
|     |                                            |                                                                             |
| 24  | (reserved)                                |                                                                             |
| 23  | (reserved)                                |                                                                             |
| 22  | H264_DMA_IN_ECC_AES_EN_CH1                |                                                                             |
| 21  | H264_DMA_IN_MEM_BURST_LENGTH_CH1          |                                                                             |
| 20  | H264_DMA_IN_CHECK_OWNER_CH1               |                                                                             |
| 19  | H264_DMA_IN_ECC_AES_EN_CH1                |                                                                             |
| 18  | (reserved)                                |                                                                             |
| 17  | H264_DMA_IN_PAGE_BOUND_EN_CH1             |                                                                             |
| 16  | (reserved)                                |                                                                             |
| 15  | H264_DMA_IN_RST_CH1                       |                                                                             |
| 14  | (reserved)                                |                                                                             |
| 13  | (reserved)                                |                                                                             |
| 12  | (reserved)                                |                                                                             |
| 11  | (reserved)                                |                                                                             |
| 10  | H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH1        |                                                                             |
| 9   | H264_DMA_IN_CMD_DISABLE_CH1               |                                                                             |
| 8   | H264_DMA_IN_RST_CH1                       |                                                                             |
| 7   | (reserved)                                |                                                                             |
| 6   | (reserved)                                |                                                                             |
| 5   | (reserved)                                |                                                                             |
| 4   | (reserved)                                |                                                                             |
| 3   | (reserved)                                |                                                                             |
| 2   | (reserved)                                |                                                                             |
| 1   | (reserved)                                |                                                                             |
| 0   | Reset                                     | 0x0                                                                           |

H264_DMA_INDSCR_BURST_EN_CH1 Configures whether to enable INCR burst transfer for RX channel 1 to read descriptors.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ECC_AES_EN_CH1 Configures whether DMA can access external memory space for ECC and AES via RX channel 1.
O: Not access
1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_IN_CHECK_OWNER_CH1 Configures whether to enable owner bit check for RX channel 1.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_MEM_BURST_LENGTH_CH1 Configures the burst length for RX channel 1.
O: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
5 ~ 7: Invalid
(R/W)

H264_DMA_IN_PAGE_BOUND_EN_CH1 Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
O: AXI read data can cross the address boundary
1: AXI read data doesn't cross the address boundary
(R/W)

H264_DMA_IN_RST_CH1 Write 1 then write 0 to reset RX channel 1. (R/W)

Continued on the next page...
```