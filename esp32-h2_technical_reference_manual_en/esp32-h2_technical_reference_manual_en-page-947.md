

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | PCNT_CNT_THR_ZERO_LAT_UO                                                   |
| 29  | PCNT_CNT_THR_H_LIM_LAT_UO                                                  |
| 28  | PCNT_CNT_THR_L_LIM_LAT_UO                                                  |
| 27  | PCNT_CNT_THR_THRES0_LAT_UO                                                 |
| 26  | PCNT_CNT_THR_THRES1_LAT_UO                                                 |
| 25  | PCNT_CNT_THR_ZERO_MODE_UO                                                  |
| 24  | Reset                                                                       |
| ... |                                                                             |
| 8   | 0x0                                                                         |
| 7   |                                                                             |
| 6   |                                                                             |
| 5   |                                                                             |
| 4   |                                                                             |
| 3   |                                                                             |
| 2   |                                                                             |
| 1   |                                                                             |
| 0   |                                                                             |

Register 32.6. PCNT_Un_STATUS_REG (n: 0-3) (0x0050+0x4*n)

PCNT_CNT_THR_ZERO_MODE_Un Represents the pulse counter status of PCNT_Un corresponding to 0.
0: The pulse counter decreases from positive to 0
1: The pulse counter increases from negative to 0
2: The pulse counter is negative
3: The pulse counter is positive (RO)

PCNT_CNT_THR_THRES1_LAT_Un Represents the latched value of thres1 event of PCNT_Un when threshold event interrupt is valid.
0: Others
1: The current pulse counter equals to thres1 and the thres1 event is valid (RO)

PCNT_CNT_THR_THRES0_LAT_Un Represents the latched value of thres0 event of PCNT_Un when threshold event interrupt is valid.
0: Others
1: The current pulse counter equals to thres0 and the thres0 event is valid (RO)

PCNT_CNT_THR_L_LIM_LAT_Un Represents the latched value of the low limit event of PCNT_Un when the threshold event interrupt is valid.
0: Others
1: The current pulse counter equals to thr_l_lim and the low limit event is valid. (RO)

PCNT_CNT_THR_H_LIM_LAT_Un Represents the latched value of the high limit event of PCNT_Un when the threshold event interrupt is valid.
0: Others
1: The current pulse counter equals to thr_h_lim and the high limit event is valid. (RO)

PCNT_CNT_THR_ZERO_LAT_Un Represents the latched value of the zero threshold event of PCNT_Un when the threshold event interrupt is valid.
0: Others
1: The current pulse counter equals to 0 and the zero threshold event is valid. (RO)
```