

```markdown
Chapter 48 Pulse Count Controller (PCNT) GoBack

Register 48.6. PCNT_Un_STATUS_REG (n: 0-3) (0x0050+0x4*n)

(reserved)
31 | 7 6 5 4 3 2 1 0
----------------------------------------------------------------------------------------------------
0 | 0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0x0 Reset

PCNT_CNT_THR_ZERO_MODE_Un Represents the pulse counter status of PCNT_Un corresponding to 0.
- 0: pulse counter decreases from positive to 0
- 1: pulse counter increases from negative to 0
- 2: pulse counter is negative
- 3: pulse counter is positive (RO)

PCNT_CNT_THR_THRES1_LAT_Un Represents whether the current value of PCNT_Un equals to thres1 when thres1 comparator is enabled.
- 0: others
- 1: the current pulse counter equals to thres1 and thres1 event is valid (RO)

PCNT_CNT_THR_THRES0_LAT_Un Represents whether the current value of PCNT_Un equals to thres0 when thres0 comparator is enabled.
- 0: others
- 1: the current pulse counter equals to thres0 and thres0 event is valid (RO)

PCNT_CNT_THR_L_LIM_LAT_Un Represents whether the current value of PCNT_Un is equal to the low limit threshold when the low limit comparator is enabled.
- 0: others
- 1: the current pulse counter equals to thr_l_lim and low limit event is valid. (RO)

PCNT_CNT_THR_H_LIM_LAT_Un Represents whether the current value of PCNT_Un is equal to the high limit threshold when the high limit comparator is enabled.
- 0: others
- 1: the current pulse counter equals to thr_h_lim and high limit event is valid. (RO)

PCNT_CNT_THR_ZERO_LAT_Un Represents whether the current value of PCNT_Un is 0 when the over-zero comparator is enabled.
- 0: others
- 1: the current pulse counter equals to 0 and zero threshold event is valid. (RO)
```