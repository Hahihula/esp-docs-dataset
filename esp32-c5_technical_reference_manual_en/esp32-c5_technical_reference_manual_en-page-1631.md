
```markdown
Register 42.10. RMT_INT_ST_REG (0x003C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                    |
| 30  | RMT_CHn_TX_LOOP_INT_ST                                                     |
| 29  | RMT_CHn_TX_THR_EVENT_INT_ST                                                |
| 28  | RMT_CHn_TX_THR_ERR_INT_ST                                                  |
| 27  | RMT_CHm_RX_END_INT_ST                                                       |
| 26  | RMT_CHm_RX_THR_EVENT_INT_ST                                                 |
| 25  | RMT_CHm_RX_THR_ERR_INT_ST                                                   |
| 24  | RMT_CHn_TX_END_INT_ST                                                        |
| 23  | RMT_CHn_ERR_INT_ST                                                           |
| 22-0| reserved                                                                     |

RMT_CHn_TX_END_INT_ST (n: 0-1) The masked interrupt status of RMT_CHn_TX_END_INT. (RO)
RMT_CHm_RX_END_INT_ST (m: 2-3) The masked interrupt status of RMT_CHm_RX_END_INT. (RO)
RMT_CHn_ERR_INT_ST (n: 0-3) The masked interrupt status of RMT_CHn/m_ERR_INT. (RO)
RMT_CHn_TX_THR_EVENT_INT_ST (n: 0-1) The masked interrupt status of RMT_CHn_TX_THR_EVENT_INT. (RO)
RMT_CHm_RX_THR_EVENT_INT_ST (m: 2-3) The masked interrupt status of RMT_CHm_RX_THR_EVENT_INT. (RO)
RMT_CHn_TX_LOOP_INT_ST (n: 0-1) The masked interrupt status of RMT_CHn_TX_LOOP_INT. (RO)
```