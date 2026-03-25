

```markdown
Chapter 36 Pulse Count Controller (PCNT)

Register 36.7 PCNT_Un_STATUS_REG (n: 0-3) (0x0060+0x4*n)

Continued from the previous page...

PCNT_CNT_THR_H_STEP_LAT_Un Represents the latched value of step counter event of PCNT_Un when step counter event interrupt is valid.
1: The current pulse counter decrement equals to reg_cnt_step and step counter event is valid.
0: Others
(RO)

PCNT_CNT_THR_L_STEP_LAT_Un Represents the latched value of step counter event of PCNT_Un when step counter event interrupt is valid.
1: The current pulse counter increment equals to reg_cnt_step and step counter event is valid.
0: Others
(RO)

Register 36.8 PCNT_INT_RAW_REG (0x0050)

PCNT_CNT_THR_EVENT_Un_INT_RAW (n: 0-3) The raw interrupt status bit for the PCNT_CNT_THR_EVENT_Un_INT interrupt. (R/WTC/SS)

Register 36.9 PCNT_INT_ST_REG (0x0054)

PCNT_CNT_THR_EVENT_Un_INT_ST (n: 0-3) The masked interrupt status bit for the PCNT_CNT_THR_EVENT_Un_INT interrupt. (RO)
```