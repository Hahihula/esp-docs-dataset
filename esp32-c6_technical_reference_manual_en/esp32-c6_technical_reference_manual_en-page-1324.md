
```markdown
Register 37.10. RMT_INT_ST_REG (0x003C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                       |                                                                             |
| 30  | RMT_CHn_TX_END_INT_ST          | The masked interrupt status of RMT_CHn_TX_END_INT. (RO)                      |
| 29  | RMT_Chm_RX_END_INT_ST          | The masked interrupt status of RMT_Chm_RX_END_INT. (RO)                      |
| 28  | RMT_Chn/m_ERR_INT_ST           | The masked interrupt status of RMT_Chn/m_ERR_INT. (RO)                       |
| 27  | RMT_CHn_TX_THR_EVENT_INT_ST    | The masked interrupt status of RMT_CHn_TX_THR_EVENT_INT. (RO)                |
| 26  | RMT_Chm_RX_THR_EVENT_INT_ST    | The masked interrupt status of RMT_Chm_RX_THR_EVENT_INT. (RO)                |
| 25  | RMT_CHn_TX_LOOP_INT_ST         | The masked interrupt status of RMT_CHn_TX_LOOP_INT. (RO)                     |

Register 37.11. RMT_INT_ENA_REG (0x0040)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                       |                                                                             |
| 30  | RMT_CHn_TX_END_INT_ENA         | Write 1 to enable RMT_CHn_TX_END_INT. (R/W)                                 |
| 29  | RMT_Chm_RX_END_INT_ENA         | Write 1 to enable RMT_Chm_RX_END_INT. (R/W)                                 |
| 28  | RMT_Chn/m_ERR_INT_ENA          | Write 1 to enable RMT_Chn/m_ERR_INT. (R/W)                                  |
| 27  | RMT_CHn_TX_THR_EVENT_INT_ENA   | Write 1 to enable RMT_CHn_TX_THR_EVENT_INT. (R/W)                           |
| 26  | RMT_Chm_RX_THR_EVENT_INT_ENA   | Write 1 to enable RMT_Chm_RX_THR_EVENT_INT. (R/W)                           |
| 25  | RMT_CHn_TX_LOOP_INT_ENA        | Write 1 to enable RMT_CHn_TX_LOOP_INT. (R/W)                                |
```