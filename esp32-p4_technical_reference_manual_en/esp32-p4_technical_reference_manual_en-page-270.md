

```markdown
Register 4.11. AHB_DMA_IN_CONFO_CHn_REG (n: 0-2) (0x0070+0xC0*n)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | AHB_DMA_IN_RST_CHn                         | Write 1 and then 0 to reset RX channel n FSM and RX FIFO pointer.(R/W)      |
| 29  | AHB_DMA_IN_LOOP_TEST_CHn                   | Reserved. (R/W)                                                             |
| 28  | AHB_DMA_INDSCR_BURST_EN_CHn                | Configures whether to enable INCR burst transfer for PX channel n to read descriptors.<br>0: Disable<br>1: Enable<br>(R/W) |
| 27  | AHB_DMA_IN_DATA_BURST_EN_CHn               | Configures whether to enable INCR burst transfer for RX channel n.<br>0: Disable<br>1: Enable<br>(R/W) |
| 26  | AHB_DMA_MEM_TRANS_EN_CHn (n = 1 ~2)        | Configures whether to enable memory-to-memory data transfer. Channel 0 does not support this feature.<br>0: Disable<br>1: Enable<br>(R/W) |
| 25  | AHB_DMA_IN_ETM_EN_CHn                      | Configures whether to enable ETM control for RX channel n.<br>0: Disable<br>1: Enable<br>(R/W) |

```