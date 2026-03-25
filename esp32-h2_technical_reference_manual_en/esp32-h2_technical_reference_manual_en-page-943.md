

```markdown
Chapter 32 Pulse Count Controller (PCNT)

GoBack

## 32.5 Registers

The addresses in this section are relative to Pulse Count Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 32.1. PCNT_Un_CONFO_REG (n: 0-3) (0x0000+0xC*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | Ox0 | O | O | 1 | 1 | 1 | 1 | 1 | 1 | Ox0 | Reset |

PCNT_FILTER_THRES_Un Configures the maximum threshold for the filter. Any pulses with width less than this will be ignored when the filter is enabled.
Measurement unit: APB_CLK cycles.
(R/W)

PCNT_FILTER_EN_Un This is the enable bit for unit n's input filter. (R/W)

PCNT_THR_ZERO_EN_Un This is the enable bit for unit n's zero comparator. (R/W)

PCNT_THR_H_LIM_EN_Un This is the enable bit for unit n's thr_h_lim comparator. Configures it to enable the high limit interrupt. (R/W)

PCNT_THR_L_LIM_EN_Un This is the enable bit for unit n's thr_l_lim comparator. Configures it to enable the low limit interrupt. (R/W)

PCNT_THR_THRESO_EN_Un This is the enable bit for unit n's thres0 comparator. (R/W)

PCNT_THR_THRES1_EN_Un This is the enable bit for unit n's thres1 comparator. (R/W)

PCNT_CHO_NEG_MODE_Un Configures the behavior when the signal input of channel 0 detects a negative edge.
1: Increment the counter
2: Decrement the counter
0, 3: No effect
(R/W)

PCNT_CHO_POS_MODE_Un Configures the behavior when the signal input of channel 0 detects a positive edge.
1: Increment the counter
2: Decrement the counter
0, 3: No effect
(R/W)

Continued on the next page...
```