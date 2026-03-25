

```markdown
- Updates pr and waits for the next sampling. The pointer pr counts cyclically between 0 and APB_SARADC_SAR_PATT_LEN (table_length).

### 33.5.8 Pattern Table

FSM contains a pattern table consisting of the `APB_SARADC_SAR_PATT_TAB1_REG` and `APB_SARADC_SAR_PATT_TAB2_REG` registers. Each register contains four patterns and each pattern is 6 bits wide, as Figure 33.5-3 and Figure 33.5-4 show.

Figure 33.5-3. APB_SARADC_SAR_PATT_TAB1_REG Contains Patterns 0 - 3

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|---|---|---|
| 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |    |    |    |

cmd x represents patterns 0 ~ 3.

Figure 33.5-4. APB_SARADC_SAR_PATT_TAB2_REG Contains Patterns 4 - 7

| 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|---|---|---|
| 0 | 0 | 0 | 0 | 0x0000 | 0x0000 | 0x0000 |    |    |    |

cmd x represents patterns 4 ~ 7.

Each pattern is 6 bits wide, consisting of three fields where conversion rules are stored. Figure 33.5-5 shows the pattern format and is followed by the descriptions of each field.

Figure 33.5-5. Pattern Structure

| 5 | 4 | 2 | 1 | 0 |
|---|---|---|---|---|
| (reserved) | ch_sel | atten |

atten Configures attenuation:
0: 0 dB
1: 2.5 dB
2: 6 dB
3: 12 dB

ch_sel Configures channel:
0: Channel 0
1: Channel 1
2: Channel 2
3: Channel 3

(reserved) Reserved
```