

Chapter 43 SPI Controller (SPI)  
GoBack

Table 43.10-2 – cont’d from previous page

| Register          | Field                     | GP-SPI2 | GP-SPI3 | LP-SPI |
|-------------------|---------------------------|---------|---------|--------|
|                   | DMA_OUTFIFO_EMPTY         | Y       | Y       | –      |
|                   | DMA_INFIFO_FULL           | Y       | Y       | –      |
|                   | DMA_SLV_SEG_TRAN_EN_Y     | Y       | Y       | –      |
|                   | SLV_RX_SEG_TRAN_CLR_EN    | Y       | Y       | –      |
| DMA_CONF_REG      | SLV_TX_SEG_TRAN_CLR_EN    | Y       | Y       | –      |
|                   | RX_EOF_EN                 | Y       | Y       | –      |
|                   | DMA_RX_ENA                | Y       | Y       | –      |
|                   | DMA_TX_ENA                | Y       | Y       | –      |
|                   | DMA_AFIFO_RST             | Y       | Y       | –      |
|                   | SLV_WK_CHARO              | —       | —       | Y      |
|                   | SLV_WK_CHAR_NUM           | —       | —       | Y      |
|                   | SLV_WK_CHAR_MASK          | —       | —       | Y      |
| SLEEP_CONFO_REG   | SLV_WK_MODE_SEL           | —       | —       | Y      |
|                   | SLEEP_EN                  | —       | —       | Y      |
|                   | SLEEP_DIS_RXFIFO_WR_EN    | —       | —       | Y      |
|                   | SLEEP_WK_DATA_SEL         | —       | —       | Y      |
|                   | SLV_WK_CHAR1              | —       | —       | Y      |
|                   | SLV_WK_CHAR2              | —       | —       | Y      |
| SLEEP_CONF1_REG   | SLV_WK_CHAR3              | —       | —       | Y      |
|                   | SLV_WK_CHAR4              | —       | —       | Y      |
|                   | SLV_RDDMA_BITLEN_EN       | Y       | Y       | –      |
|                   | SLV_WRDMA_BITLEN_EN       | Y       | Y       | –      |
| SLAVE_REG         | SLV_LAST_BYTE_STRB        | Y       | Y       | –      |
|                   | DMA_SEG_MAGIC_VALUE       | Y       | —       | –      |
|                   | USR_CONF                  | Y       | —       | –      |
|                   | MST_FD_WAIT_DMA_TX_DATA   | Y       | —       | –      |
| DIN_MODE_REG      | DIN4_MODE                 | Y       | —       | –      |
|                   | DIN5_MODE                 | Y       | —       | –      |
|                   | DIN6_MODE                 | Y       | —       | –      |
|                   | DIN7_MODE                 | Y       | —       | –      |
|                   | DIN4_NUM                  | Y       | —       | –      |
| DIN_NUM_REG       | DIN5_NUM                  | Y       | —       | –      |
|                   | DIN6_NUM                  | Y       | —       | –      |
|                   | DIN7_NUM                  | Y       | —       | –      |
| DOUT_MODE_REG     | DOUT4_MODE                | Y       | —       | –      |
|                   | DOUT5_MODE                | Y       | —       | –      |
|                   | DOUT6_MODE                | Y       | —       | –      |
|                   | DOUT7_MODE                | Y       | —       | –      |
|                   | D_LDQS_MODE               | Y       | —       | –      |

Cont’d on next page

Espressif Systems    2243    ESP32-P4 TRM PRELIMINARY Submit Documentation Feedback