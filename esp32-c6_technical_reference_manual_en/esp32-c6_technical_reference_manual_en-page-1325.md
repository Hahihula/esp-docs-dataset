
```markdown
Register 37.12. RMT_INT_CLR_REG (0x0044)

| Bit 31 | Bit 30 | ... | Bit 9 | Bit 8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|--------|-----|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
|        |        |     |       |       |       |       |       |       |       | Reset |       |       |

RMT_CHn_TX_END_INT_CLR  Write 1 to clear RMT_CHn_TX_END_INT. (WT)
RMT_Chm_RX_END_INT_CLR  Write 1 to clear RMT_Chm_RX_END_INT. (WT)
RMT_Chn/m_ERR_INT_CLR   Write 1 to clear RMT_Chn/m_ERR_INT. (WT)
RMT_CHn_TX_THR_EVENT_INT_CLR  Write 1 to clear RMT_CHn_TX_THR_EVENT_INT. (WT)
RMT_Chm_RX_THR_EVENT_INT_CLR  Write 1 to clear RMT_Chm_RX_THR_EVENT_INT. (WT)
RMT_CHn_TX_LOOP_INT_CLR   Write 1 to clear RMT_CHn_TX_LOOP_INT. (WT)

Register 37.13. RMT_CHn_CARRIER_DUTY_REG (n: 0-1) (0x0048+0x4*n)

| Bit 31 | Bit 16 | Bit 15 | ... | Bit 0 |
|--------|--------|--------|-----|-------|
|        |        |        |     | Reset |

RMT_CARRIER_LOW_CHn   Configures carrier wave's low level clock period for channel n.
Measurement unit: rmt_sclk
(R/W)

RMT_CARRIER_HIGH_CHn  Configures carrier wave's high level clock period for channel n.
Measurement unit: rmt_sclk
(R/W)
```