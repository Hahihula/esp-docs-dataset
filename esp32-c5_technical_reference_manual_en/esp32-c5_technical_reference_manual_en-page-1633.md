
```markdown
Register 42.12. RMT_INT_CLR_REG (0x0044)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 14  | RMT_CH1_TX_LOOP_INT_CLR                                                     |
| 13  | RMT_CH0_TX_LOOP_INT_CLR                                                     |
| 12  | RMT_CH3_RX_THR_EVENT_INT_CLR                                                |
| 11  | RMT_CH2_RX_THR_EVENT_INT_CLR                                                |
| 10  | RMT_CH1_RX_THR_EVENT_INT_CLR                                                |
| 9   | RMT_CH0_RX_THR_EVENT_INT_CLR                                                |
| 8   | RMT_CH3_ERR_INT_CLR                                                         |
| 7   | RMT_CH2_ERR_INT_CLR                                                         |
| 6   | RMT_CH1_ERR_INT_CLR                                                         |
| 5   | RMT_CH0_ERR_INT_CLR                                                         |
| 4   | RMT_CH3_RX_END_INT_CLR                                                      |
| 3   | RMT_CH2_RX_END_INT_CLR                                                      |
| 2   | RMT_CH1_RX_END_INT_CLR                                                      |
| 1   | RMT_CH0_RX_END_INT_CLR                                                      |
| 0   | Reset                                                                      |

RMT_CHn_TX_END_INT_CLR (n: 0-1) Write 1 to clear the RMT_CHn_TX_END_INT interrupt. (WT)
RMT_CHm_RX_END_INT_CLR (m: 2-3) Write 1 to clear the RMT_CHm_RX_END_INT interrupt. (WT)

RMT_CHn_ERR_INT_CLR (n: 0-3) Write 1 to clear the RMT_CHn/m_ERR_INT interrupt. (WT)
RMT_CHn_TX_THR_EVENT_INT_CLR (n: 0-1) Write 1 to clear the RMT_CHn_TX_THR_EVENT_INT interrupt. (WT)
RMT_CHm_RX_THR_EVENT_INT_CLR (m: 2-3) Write 1 to clear the RMT_CHm_RX_THR_EVENT_INT interrupt. (WT)
RMT_CHn_TX_LOOP_INT_CLR (n: 0-1) Write 1 to clear the RMT_CHn_TX_LOOP_INT interrupt. (WT)

Register 42.13. RMT_CHnCARRIER_DUTY_REG (n: 0-1) (0x0048+0x4*n)
```