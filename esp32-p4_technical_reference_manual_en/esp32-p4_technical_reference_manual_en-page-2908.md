

```markdown
Register 57.11. RMT_INT_RAW_REG (0x0070)

31   30   29   28   27   26   25   24   23   22   21   20   19   18   17   16   15   14   13   12   11   10   9    8    7    6    5    4    3    2    1    0
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0    0 | Reset

RMT_CHn_TX_END_INT_RAW (n: 0-3) The raw interrupt status of RMT_CHn_TX_END_INT.
(R/WTC/SS)

RMT_CHn_ERR_INT_RAW (n: 0-3) The raw interrupt status of RMT_CHn_ERR_INT. (R/WTC/SS)

RMT_CHn_TX_THR_EVENT_INT_RAW (n: 0-3) The raw interrupt status of
RMT_CHn_TX_THR_EVENT_INT. (R/WTC/SS)

RMT_CHn_TX_LOOP_INT_RAW (n: 0-3) The raw interrupt status of RMT_CHn_TX_LOOP_INT.
(R/WTC/SS)

RMT_Chm_RX_END_INT_RAW (m: 4-7) The raw interrupt status of RMT_Chm_RX_END_INT.
(R/WTC/SS)

RMT_Chm_ERR_INT_RAW (m: 4-7) The raw interrupt status of RMT_Chm_ERR_INT. (R/WTC/SS)

RMT_Chm_RX_THR_EVENT_INT_RAW (m: 4-7) The raw interrupt status of
RMT_Chm_RX_THR_EVENT_INT. (R/WTC/SS)

RMT_CHn_DMA_ACCESS_FAIL_INT_RAW (n: 3) The raw interrupt status of
RMT_CHn_DMA_ACCESS_FAIL_INT. (R/WTC/SS)

RMT_Chm_DMA_ACCESS_FAIL_INT_RAW (m: 7) The raw interrupt status of
RMT_Chm_DMA_ACCESS_FAIL_INT. (R/WTC/SS)
```