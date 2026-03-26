

```markdown
Register 39.129. H264_DMA_COUNTER_RST_REG (0x0B50)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 4   | Reset                                      |                                                                             |
| 3   | H264_DMA_RX_CH5_INTER_COUNTER_RST          | Write 1 then write 0 to reset RX ch5 counter. (R/W)                         |
| 2   | H264_DMA_RX_CH2_INTER_COUNTER_RST          | Write 1 then write 0 to reset RX ch2 counter. (R/W)                         |
| 1   | H264_DMA_RX_CH1_EXTERN_COUNTER_RST         | Write 1 then write 0 to reset RX ch1 counter. (R/W)                         |
| 0   | H264_DMA_RX_CHO_EXTERN_COUNTER_RST         | Write 1 then write 0 to reset RX ch0 counter. (R/W)                         |

```
```markdown
H264_DMA_RX_CHO_EXTERN_COUNTER_RST    Write 1 then write 0 to reset RX ch0 counter. (R/W)
H264_DMA_RX_CH1_EXTERN_COUNTER_RST    Write 1 then write 0 to reset RX ch1 counter. (R/W)
H264_DMA_RX_CH2_INTER_COUNTER_RST     Write 1 then write 0 to reset RX ch2 counter. (R/W)
H264_DMA_RX_CH5_INTER_COUNTER_RST     Write 1 then write 0 to reset RX ch5 counter. (R/W)
```