

```markdown
Register 39.112. H264_DMA_IN_CONFO_CH5_REG (0x0A00)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            | (reserved)                                                                  |
| 30  |                                            | (reserved)                                                                  |
| 29  | H264_DMA_IN_CMD_DISABLE_CH5               | Configures whether to disable command on RX channel 5.                      |
| 28  | H264_DMA_IN_RST_CH5                       | Write 1 then write 0 to reset RX channel 5. (R/W)                           |
| 27  |                                            | (reserved)                                                                  |
| 26  |                                            | (reserved)                                                                  |
| 25  |                                            | (reserved)                                                                  |
| 24  | H264_DMA_IN_PAGE_BOUND_EN_CH5             | Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length. <br>0: AXI read data can cross the address boundary <br>1: AXI read data doesn't cross the address boundary (R/W) |
| 23  | H264_DMA_IN_MEM_BURST_LENGTH_CH5          | Configures the burst length for RX channel 5. <br>0: 8 bytes <br>1: 16 bytes <br>2: 32 bytes <br>3: 64 bytes <br>4: 128 bytes <br>5 ~ 7: Invalid (R/W) |
| 22  |                                            | (reserved)                                                                  |
| 21  | H264_DMA_IN_ECC_AES_EN_CH5                | Configures whether DMA can access external memory space for ECC and AES via RX channel 5. <br>0: Not access <br>1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned. (R/W) |
| 20  |                                            | (reserved)                                                                  |
| 19  |                                            | (reserved)                                                                  |
| 18  |                                            | (reserved)                                                                  |
| 17  |                                            | (reserved)                                                                  |
| 16  |                                            | (reserved)                                                                  |
| 15  |                                            | (reserved)                                                                  |
| 14  |                                            | (reserved)                                                                  |
| 13  |                                            | (reserved)                                                                  |
| 12  |                                            | (reserved)                                                                  |
| 11  |                                            | (reserved)                                                                  |
| 10  |                                            | (reserved)                                                                  |
| 9   |                                            | (reserved)                                                                  |
| 8   |                                            | (reserved)                                                                  |
| 7   |                                            | (reserved)                                                                  |
| 6   |                                            | (reserved)                                                                  |
| 5   |                                            | (reserved)                                                                  |
| 4   |                                            | (reserved)                                                                  |
| 3   |                                            | (reserved)                                                                  |
| 2   |                                            | (reserved)                                                                  |
| 1   |                                            | (reserved)                                                                  |
| 0   | Reset                                     | 0x0                                                                          |

H264_DMA_IN_ECC_AES_EN_CH5 Configures whether DMA can access external memory space for ECC and AES via RX channel 5.
- 0: Not access
- 1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned. (R/W)

H264_DMA_IN_MEM_BURST_LENGTH_CH5 Configures the burst length for RX channel 5.
- 0: 8 bytes
- 1: 16 bytes
- 2: 32 bytes
- 3: 64 bytes
- 4: 128 bytes
- 5 ~ 7: Invalid (R/W)

H264_DMA_IN_PAGE_BOUND_EN_CH5 Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
- 0: AXI read data can cross the address boundary
- 1: AXI read data doesn't cross the address boundary (R/W)

H264_DMA_IN_RST_CH5 Write 1 then write 0 to reset RX channel 5. (R/W)

H264_DMA_IN_CMD_DISABLE_CH5 Configures whether to disable command on RX channel 5.
- 0: Disable
- 1: Enable (R/W)
```