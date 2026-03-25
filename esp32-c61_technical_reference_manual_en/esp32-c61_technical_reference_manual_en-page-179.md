

```markdown
Register 3.10. AHB_DMA_IN_CONFO_CHn_REG (n: 0-1) (0x0070+0xC0*n)

| Bit | Field Name                                 | Description                                                                                                                                                                                                 |
|-----|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                                                                                                                                                           |
| 30  | AHB_DMA_IN_RST_CHn                         | Write 1 and then 0 to reset RX channel n FSM and RX FIFO pointer. (R/W)                                                                                                                                     |
| 29  | AHB_DMA_IN_LOOP_TEST_CHn                   | Configures the owner bit value for inline write-back. (R/W)                                                                                                                                                  |
| 28  | AHB_DMA_INDSCR_BURST_EN_CHn                | Configures whether to enable INCR burst transfer for RX channel n to read descriptors.<br>0: Disable<br>1: Enable<br>(R/W)                                                                                   |
| 27  | AHB_DMA_MEM_TRANS_EN_CHn                   | Configures whether to enable memory-to-memory data transfer.<br>0: Disable<br>1: Enable<br>(R/W)                                                                                                               |
| 26  | AHB_DMA_IN_ETM_EN_CHn                      | Configures whether to enable ETM control for RX channel n.<br>0: Disable<br>1: Enable<br>(R/W)                                                                                                                |
| 25  | AHB_DMA_IN_DATA_BURST_MODE_SEL_CHn         | Configures maximum burst length for RX channel n.<br>0: SINGLE<br>1: INCR4<br>2: INCR8<br>3: Reserved<br>(R/W)                                                                                                 |

```
```markdown
AHB_DMA_IN_RST_CHn Write 1 and then 0 to reset RX channel n FSM and RX FIFO pointer. (R/W)

AHB_DMA_IN_LOOP_TEST_CHn Configures the owner bit value for inline write-back. (R/W)

AHB_DMA_INDSCR_BURST_EN_CHn Configures whether to enable INCR burst transfer for RX channel n to read descriptors.
0: Disable
1: Enable
(R/W)

AHB_DMA_MEM_TRANS_EN_CHn Configures whether to enable memory-to-memory data transfer.
0: Disable
1: Enable
(R/W)

AHB_DMA_IN_ETM_EN_CHn Configures whether to enable ETM control for RX channel n.
0: Disable
1: Enable
(R/W)

AHB_DMA_IN_DATA_BURST_MODE_SEL_CHn Configures maximum burst length for RX channel n.
0: SINGLE
1: INCR4
2: INCR8
3: Reserved
(R/W)
```