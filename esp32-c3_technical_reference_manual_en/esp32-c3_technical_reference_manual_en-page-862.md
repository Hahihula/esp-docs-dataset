

```markdown
Register 33.12. RMT_INT_ENA_REG (0x0040)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 30  |                                 | Reset                                                                      |
| 29  |                                 | Reset                                                                      |
| ... |                                 | ...                                                                        |
| 7   | RMT_CH1_TX_LOOP_INT_ENA        | The interrupt enable bit for RMT_CH1_TX_LOOP_INT. (R/W)                     |
| 6   | RMT_CH0_TX_LOOP_INT_ENA        | The interrupt enable bit for RMT_CH0_TX_LOOP_INT. (R/W)                     |
| 5   | RMT_CH3_RX_THR_EVENT_INT_ENA   | The interrupt enable bit for RMT_CH3_RX_THR_EVENT_INT. (R/W)                |
| 4   | RMT_CH2_RX_THR_EVENT_INT_ENA   | The interrupt enable bit for RMT_CH2_RX_THR_EVENT_INT. (R/W)                |
| 3   | RMT_CH1_TX_THR_EVENT_INT_ENA   | The interrupt enable bit for RMT_CH1_TX_THR_EVENT_INT. (R/W)                |
| 2   | RMT_CH3_ERR_INT_ENA            | The interrupt enable bit for RMT_CH3_ERR_INT. (R/W)                         |
| 1   | RMT_CH2_ERR_INT_ENA            | The interrupt enable bit for RMT_CH2_ERR_INT. (R/W)                         |
| 0   | RMT_CH1_ERR_INT_ENA            | The interrupt enable bit for RMT_CH1_ERR_INT. (R/W)                         |

RMT_CHO_TX_END_INT_ENA    The interrupt enable bit for RMT_CHO_TX_END_INT. (R/W)
RMT_CH1_TX_END_INT_ENA    The interrupt enable bit for RMT_CH1_TX_END_INT. (R/W)
RMT_CH2_RX_END_INT_ENA    The interrupt enable bit for RMT_CH2_RX_END_INT. (R/W)
RMT_CH3_RX_END_INT_ENA    The interrupt enable bit for RMT_CH3_RX_END_INT. (R/W)
RMT_CHO_ERR_INT_ENA       The interrupt enable bit for RMT_CHO_ERR_INT. (R/W)
RMT_CH1_ERR_INT_ENA       The interrupt enable bit for RMT_CH1_ERR_INT. (R/W)
RMT_CH2_ERR_INT_ENA       The interrupt enable bit for RMT_CH2_ERR_INT. (R/W)
RMT_CH3_ERR_INT_ENA       The interrupt enable bit for RMT_CH3_ERR_INT. (R/W)
RMT_CHO_TX_THR_EVENT_INT_ENA    The interrupt enable bit for RMT_CHO_TX_THR_EVENT_INT. (R/W)
RMT_CH1_TX_THR_EVENT_INT_ENA    The interrupt enable bit for RMT_CH1_TX_THR_EVENT_INT. (R/W)
RMT_CH2_RX_THR_EVENT_INT_ENA    The interrupt enable bit for RMT_CH2_RX_THR_EVENT_INT. (R/W)
RMT_CH3_RX_THR_EVENT_INT_ENA    The interrupt enable bit for RMT_CH3_RX_THR_EVENT_INT. (R/W)
RMT_CHO_TX_LOOP_INT_ENA         The interrupt enable bit for RMT_CHO_TX_LOOP_INT. (R/W)
RMT_CH1_TX_LOOP_INT_ENA         The interrupt enable bit for RMT_CH1_TX_LOOP_INT. (R/W)
```