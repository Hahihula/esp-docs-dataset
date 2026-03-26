

```markdown
Register 39.107. H264_DMA_IN_CONFO_CH4_REG (0x0900)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH4         | Configures whether to enable INCR burst transfer for RX channel 4 to read descriptors. |
|     |                                             | O: Disable<br>1: Enable<br>(R/W)                                           |
| 29  | H264_DMA_IN_CMD_DISABLE_CH4                |                                                                             |
| 28  | H264_DMA_IN_RST_CH4                        | Write 1 then write 0 to reset RX channel 4. (R/W)                           |
|     |                                             | O: Disable<br>1: Enable<br>(R/W)                                           |
| 27  | (reserved)                                 |                                                                             |
| 26  | H264_DMA_IN_PAGE_BOUND_EN_CH4              | Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length. |
|     |                                             | O: AXI read data can cross the address boundary<br>1: AXI read data doesn't cross the address boundary<br>(R/W) |
| 25  | H264_DMA_IN_MEM_BURST_LENGTH_CH4           | Configures the burst length for RX channel 4.<br>O: 8 bytes<br>1: 16 bytes<br>2: 32 bytes<br>3: 64 bytes<br>4: 128 bytes<br>5 ~ 7: Invalid<br>(R/W) |
| 24  | H264_DMA_IN_CHECK_OWNER_CH4                | Configures whether to enable owner bit check for RX channel 4.<br>O: Disable<br>1: Enable<br>(R/W) |
| 23  | H264_DMA_IN_ECC_AES_EN_CH4                 | Configures whether DMA can access external memory space for ECC and AES via RX channel 4.<br>O: Not access<br>1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.<br>(R/W) |
| 22  | (reserved)                                 |                                                                             |
| 13  | H264_DMA_IN_INDSOR_BURST_EN_CH4            |                                                                             |
|     |                                             | O: Disable<br>1: Enable<br>(R/W)                                           |
| 12  | (reserved)                                 |                                                                             |
| 11  | H264_DMA_IN_ECC_AES_EN_CH4                 |                                                                             |
| 10  | H264_DMA_IN_CHECK_OWNER_CH4                |                                                                             |
| 9   | H264_DMA_IN_MEM_BURST_LENGTH_CH4           |                                                                             |
| 8   | (reserved)                                 |                                                                             |
| 7   | O×0                                        | Reset                                                                        |
```