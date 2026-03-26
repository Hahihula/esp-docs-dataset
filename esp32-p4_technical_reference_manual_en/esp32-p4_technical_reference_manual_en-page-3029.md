

```markdown
When FSM receives the `reader_done` signal from HP Reader, it starts the following operations:

* Stops sampling.
* Transfers the conversion result to the filter. Then the threshold monitor transfers the filtered result to memory via GDMA (see Figure 62.4-1).
* Updates pr and waits for the next sampling. The pointer pr counts cyclically between 0 and `ADC_SAR1/2_PATT_LEN` (`table_length`).

## 62.5.6 HP ADC Pattern Table

HP ADC FSM1/2 each contain a pattern table configured by `ADC_SARx_PATT_TABm_REG`, with `m` indicating registers 1 ~ 4. Each register contains four patterns and each pattern is 6 bits wide, as below shows.

Figure 62.5-2. `ADC_SARx_PATT_TAB1_REG` Contains Patterns 0 - 3

| (reserved) | cmd0 | cmd1 | cmd2 | cmd3 |
|:-----------:|:-----:|:-----:|:-----:|:-----:|
| 31          | 24    | 18    | 12    | 6     | 0     |
| 0x0000      |       |       |       |       |

`cmd n (n = 0 - 3)` represents patterns 0 - 3.

Figure 62.5-3. `ADC_SARx_PATT_TAB2_REG` Contains Patterns 4 - 7

| (reserved) | cmd4 | cmd5 | cmd6 | cmd7 |
|:-----------:|:-----:|:-----:|:-----:|:-----:|
| 31          | 24    | 18    | 12    | 6     | 0     |
| 0x0000      |       |       |       |       |

`cmd n (n = 4 - 7)` represents patterns 4 ~ 7.

Figure 62.5-4. `ADC_SARx_PATT_TAB3_REG` Contains Patterns 8 - 11

| (reserved) | cmd8 | cmd9 | cmd10 | cmd11 |
|:-----------:|:-----:|:-----:|:------:|:------:|
| 31          | 24    | 18    | 12     | 6      | 0      |
| 0x0000      |       |       |        |        |

`cmd n (n = 8 - 11)` represents patterns 8 ~ 11.

Figure 62.5-5. `ADC_SARx_PATT_TAB4_REG` Contains Patterns 12 - 15

| (reserved) | cmd12 | cmd13 | cmd14 | cmd15 |
|:-----------:|:------:|:------:|:------:|:------:|
| 31          | 24     | 18     | 12     | 6      | 0      |
| 0x0000      |        |        |        |        |

`cmd n (n = 12 - 15)` represents patterns 12 ~ 15.
```