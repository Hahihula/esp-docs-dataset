

```markdown
## 40.5.8 Pattern Table

FSM contains a pattern table consisting of the `APB_SARADC_SAR_PATT_TAB1_REG` and `APB_SARADC_SAR_PATT_TAB2_REG` registers. Each register contains four patterns and each pattern is 6 bits wide, as Figure 40.5-3 and Figure 40.5-4 show.

Figure 40.5-3. APB_SARADC_SAR_PATT_TAB1_REG Contains Patterns 0 - 3

| Bit | 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|-----|----|----|----|----|----|----|----|---|---|---|
|     | (reserved) |    | cmd0 | cmd1 |    | cmd2 | cmd3 |   |   |   |

cmd X represents patterns 0 ~ 3.

Figure 40.5-4. APB_SARADC_SAR_PATT_TAB2_REG Contains Patterns 4 - 7

| Bit | 31 | 24 | 23 | 18 | 17 | 12 | 11 | 6 | 5 | 0 |
|-----|----|----|----|----|----|----|----|---|---|---|
|     | (reserved) |    | cmd4 | cmd5 |    | cmd6 | cmd7 |   |   |   |

cmd X represents patterns 4 ~ 7.

Each pattern is 6 bits wide, consisting of three fields where conversion rules are stored. Figure 40.5-5 shows the pattern format and is followed by the descriptions of each field.

Figure 40.5-5. Pattern Structure

| Bit | 5 | 4 | 2 | 1 | 0 |
|-----|---|---|---|---|---|
|     | (reserved) | ch_sel | atten |   |   |

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
4: Channel 4

(reserved) Reserved

Pattern Configuration Example
```