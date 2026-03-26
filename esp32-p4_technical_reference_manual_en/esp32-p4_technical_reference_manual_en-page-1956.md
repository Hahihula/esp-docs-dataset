

```markdown
Register 39.127. H264_DMA_OUT_ARB_CONFIG_REG (0x0B30)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                 |                                                                             |
| 17        | H264_DMA_OUT_WEIGHT_EN                     | Configures whether to enable weight arbitration for TX. (R/W)                |
| 16-0      | H264_DMA_OUT_ARB_TIMEOUT_NUM               | Configures the max number of timeout count of arbiter. (R/W)                 |

Register 39.128. H264_DMA_IN_ARB_CONFIG_REG (0x0B34)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                 |                                                                             |
| 17        | H264_DMA_IN_WEIGHT_EN                      | Configures whether to enable weight arbitration for RX. (R/W)                |
| 16-0      | H264_DMA_IN_ARB_TIMEOUT_NUM                | Configures the max number of timeout count of arbiter. (R/W)                 |
```