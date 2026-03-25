
```markdown
Register 37.12. RMT_INT_CLR_REG (0x0044)

| Bit  | Description                                                                 |
|------|-----------------------------------------------------------------------------|
| 31   | reserved                                                                     |
| 30-16| RMT_CH1_TX_LOOP_INT_CLR ... RMT_CH2_TX_END_INT_CLR                         |

RMT_CHn_TX_END_INT_CLR Write 1 to clear RMT_CHn_TX_END_INT. (WT)
RMT_Chm_RX_END_INT_CLR Write 1 to clear RMT_Chm_RX_END_INT. (WT)
RMT_Chn/m_ERR_INT_CLR Write 1 to clear RMT_Chn/m_ERR_INT. (WT)
RMT_CHn_TX_THR_EVENT_INT_CLR Write 1 to clear RMT_CHn_TX_THR_EVENT_INT. (WT)
RMT_Chm_RX_THR_EVENT_INT_CLR Write 1 to clear RMT_Chm_RX_THR_EVENT_INT. (WT)
RMT_CHn_TX_LOOP_INT_CLR Write 1 to clear RMT_CHn_TX_LOOP_INT. (WT)

Register 37.13. RMT_CHnCARRIER_DUTY_REG (n: 0-1) (0x0048+0x4*n)

| Bit  | Description                                                                 |
|------|-----------------------------------------------------------------------------|
| 31   | 0x40                                                                        |
| 30-16| RMT_CARRIER_HIGH_CHn ... RMT_CARRIER_LOW_CHn                                |

RMT_CARRIER_LOW_CHn Configures carrier wave's low level clock period for channel n.
Measurement unit: rmt_sclk
(R/W)

RMT_CARRIER_HIGH_CHn Configures carrier wave's high level clock period for channel n.
Measurement unit: rmt_sclk
(R/W)
```