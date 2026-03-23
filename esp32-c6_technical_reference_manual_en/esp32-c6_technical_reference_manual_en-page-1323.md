
```markdown
Register 37.9. RMT_INT_RAW_REG (0x0038)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                   |
| 30  |                             | Reset                                                                       |
| 29  |                             | Reset                                                                       |
| ... |                             | ...                                                                         |
| 8   | RMT_CHn_TX_LOOP_INT_RAW     | The raw interrupt status of RMT_CHn_TX_LOOP_INT. Triggered when the loop count reaches the configured threshold value. (R/WTC/SS) |
| 7   | RMT_CHn_TX_THR_EVENT_INT_RAW| The raw interrupt status of RMT_CHn_TX_THR_EVENT_INT. Triggered when the transmitter sent more data than the configured value. (R/WTC/SS) |
| 6   | RMT_CHm_RX_THR_EVENT_INT_RAW| The raw interrupt status of RMT_CHm_RX_THR_EVENT_INT. Triggered when the receiver receives more data than the configured value. (R/WTC/SS) |
| 5   | RMT_CHn_TX_END_INT_RAW      | The raw interrupt status of RMT_CHn_TX_END_INT. Triggered when the transmission is done. (R/WTC/SS) |
| 4   | RMT_CHm_RX_END_INT_RAW      | The raw interrupt status of RMT_CHm_RX_END_INT. Triggered when the reception is done. (R/WTC/SS) |
| 3   | RMT_CHn/m_ERR_INT_RAW       | The raw interrupt status of RMT_CHn/m_ERR_INT. Triggered when error occurs. (R/WTC/SS) |
```