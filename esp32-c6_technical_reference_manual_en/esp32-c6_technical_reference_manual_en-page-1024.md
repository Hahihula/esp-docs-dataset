

```markdown
Register 31.2. PCNT_Un_CONF1_REG (n: 0-3) (0x0004+0xC*n)

| 31 | 16   | 15       | 0         |
|----|------|----------|-----------|
|    |      |          |           |
| 0x00 | 0x00 | Reset    |

PCNT_CNT_THRESO_Un Configures the thres0 value for unit n. (R/W)
PCNT_CNT_THRESH1_Un Configures the thres1 value for unit n. (R/W)

Register 31.3. PCNT_Un_CONF2_REG (n: 0-3) (0x0008+0xC*n)

| 31 | 16   | 15       | 0         |
|----|------|----------|-----------|
|    |      |          |           |
| 0x00 | 0x00 | Reset    |

PCNT_CNT_H_LIM_Un Configures the thr_h_lim value for unit n. When pulse_cnt reaches this value, the counter will be cleared to 0. (R/W)
PCNT_CNT_L_LIM_Un Configures the thr_l_lim value for unit n. When pulse_cnt reaches this value, the counter will be cleared to 0.(R/W)
```