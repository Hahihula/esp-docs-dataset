

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| H264_DMA_OUT_DSCR_BF1_CH4_REG             | TX CH4 second-to-last dscr addr register                                   | 0x0434  | RO     |
| H264_DMA_OUT_BUF_LEN_CH4_REG              | TX CH4 buf len register                                                    | 0x0470  | RO     |
| H264_DMA_OUT_FIFO_BCNT_CH4_REG            | TX CH4 fifo byte cnt register                                              | 0x0474  | RO     |
| H264_DMA_OUT_PUSH_BYTECNT_CH4_REG         | TX CH4 push byte cnt register                                              | 0x0478  | RO     |
| H264_DMA_OUT_XADDR_CH4_REG                | TX CH4 xaddr register                                                      | 0x047C  | RO     |
| H264_DMA_OUT_BLOCK_BUF_LEN_CH4_REG        | TX CH4 block buf len register                                              | 0x0480  | RO     |

RX Status Registers
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| H264_DMA_INFIFO_STATUS_CHO_REG            | RX CHO INFIFO status register                                              | 0x0514  | RO     |
| H264_DMA_IN_STATE_CHO_REG                 | RX CHO state register                                                      | 0x0524  | RO     |
| H264_DMA_IN_SUC_EOF_DES_ADDR_CH0_REG      | RX CHO eof des addr register                                               | 0x0528  | RO     |
| H264_DMA_IN_ERR_EOF_DES_ADDR_CH0_REG      | RX CHO err eof des addr register                                           | 0x052C  | RO     |
| H264_DMA_IN_DSCR_CHO_REG                  | RX CHO next dscr addr register                                             | 0x0530  | RO     |
| H264_DMA_IN_DSCR_BFO_CH0_REG              | RX CHO last dscr addr register                                             | 0x0534  | RO     |
| H264_DMA_IN_DSCR_BF1_CH0_REG              | RX CHO second-to-last dscr addr register                                   | 0x0538  | RO     |
| H264_DMA_IN_FIFO_CNT_CHO_REG              | RX CHO fifo cnt register                                                   | 0x0580  | RO     |
| H264_DMA_IN_POP_DATA_CNT_CHO_REG          | RX CHO pop data cnt register                                               | 0x0584  | RO     |
| H264_DMA_IN_XADDR_CHO_REG                 | RX CHO xaddr register                                                      | 0x0588  | RO     |
| H264_DMA_IN_BUF_HB_RCV_CHO_REG            | RX CHO buf len hb rcv register                                             | 0x058C  | RO     |
| H264_DMA_INFIFO_STATUS_CH1_REG            | RX CH1 INFIFO status register                                              | 0x0614  | RO     |
| H264_DMA_IN_STATE_CH1_REG                 | RX CH1 state register                                                      | 0x0624  | RO     |
| H264_DMA_IN_SUC_EOF_DES_ADDR_CH1_REG      | RX CH1 eof des addr register                                               | 0x0628  | RO     |
| H264_DMA_IN_ERR_EOF_DES_ADDR_CH1_REG      | RX CH1 err eof des addr register                                           | 0x062C  | RO     |
| H264_DMA_IN_DSCR_CH1_REG                  | RX CH1 next dscr addr register                                             | 0x0630  | RO     |
| H264_DMA_IN_DSCR_BFO_CH1_REG              | RX CH1 last dscr addr register                                             | 0x0634  | RO     |
| H264_DMA_IN_DSCR_BF1_CH1_REG              | RX CH1 second-to-last dscr addr register                                   | 0x0638  | RO     |

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| H264_DMA_IN_FIFO_CNT_CH1_REG              | RX CH1 fifo cnt register                                                   | 0x0680  | RO     |
| H264_DMA_IN_POP_DATA_CNT_CH1_REG          | RX CH1 pop data cnt register                                               | 0x0684  | RO     |
| H264_DMA_IN_XADDR_CH1_REG                 | RX CH1 xaddr register                                                      | 0x0688  | RO     |
| H264_DMA_IN_BUF_HB_RCV_CH1_REG            | RX CH1 buf len hb rcv register                                             | 0x068C  | RO     |
| H264_DMA_INFIFO_STATUS_CH2_REG            | RX CH2 INFIFO status register                                              | 0x0714  | RO     |
| H264_DMA_IN_STATE_CH2_REG                 | RX CH2 state register                                                      | 0x0724  | RO     |
| H264_DMA_IN_SUC_EOF_DES_ADDR_CH2_REG      | RX CH2 eof des addr register                                               | 0x0728  | RO     |
| H264_DMA_IN_ERR_EOF_DES_ADDR_CH2_REG      | RX CH2 err eof des addr register                                           | 0x072C  | RO     |
| H264_DMA_IN_DSCR_CH2_REG                  | RX CH2 next dscr addr register                                             | 0x0730  | RO     |
| H264_DMA_IN_DSCR_BFO_CH2_REG              | RX CH2 last dscr addr register                                             | 0x0734  | RO     |
| H264_DMA_IN_DSCR_BF1_CH2_REG              | RX CH2 second-to-last dscr addr register                                   | 0x0738  | RO     |

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| H264_DMA_IN_FIFO_CNT_CH2_REG              | RX CH2 fifo cnt register                                                   | 0x0780  | RO     |
| H264_DMA_IN_POP_DATA_CNT_CH2_REG          | RX CH2 pop data cnt register                                               | 0x0784  | RO     |
| H264_DMA_IN_XADDR_CH2_REG                 | RX CH2 xaddr register                                                      | 0x0788  | RO     |
```