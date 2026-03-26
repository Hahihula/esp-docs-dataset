

```markdown
| Bit          | Description |
|--------------|-------------|
| 0-31         | The bit is sourced from bit N in the incoming FIFO register. |
| 32-63        | The source of the bit depends on the setting of CTL_CTR_SRC_SEL and CTL_LUT_SRC_SEL: <br> If CTL_CTR_SRC_SEL = 0: the bit is sourced from bit N in the incoming FIFO register. <br> If CTL_CTR_SRC_SEL = 1: the bit is sourced from bit (N-32) of the counter registers. Specifically, if N is 32 to 47, the bit is sourced from bit (N-32) of counter A and if N is 48 to 63, the bit is sourced from bit (N-48) of counter B. <br> If CTL_LUT_SRC_SEL = 1: Depending on the width of the LUT (8, 16, or 32 bits), a read of the top 8, 16, or 32 bits will return data from the LUT rather than what CTL_CTR_SRC_SEL selects. Specifically, given a LUT width of N, 63 will return LUT output bit (N-1), 62 will return LUT output bit (N-2) and so on. |
| 64           | CounterB[7:0] <= last[7:0] |
| 65           | CounterB[7:0] > last[7:0] |
| 66           | CounterB[7:0] = last[7:0] |
| 67           | CounterB[7:0] <= last[15:8] |
| 68           | CounterB[7:0] > last[15:8] |
| 69           | CounterB[7:0] = last[15:8] |
| 70           | CounterB[7:0] <= last[23:16] |
| 71           | CounterB[7:0] > last[23:16] |
| 72           | CounterB[7:0] = last[23:16] |
| 73           | CounterB[7:0] <= last[31:24] |
| 74           | CounterB[7:0] > last[31:24] |
| 75           | CounterB[7:0] = last[31:24] |
| 76           | CounterB[15:8] <= last[7:0] |
| 77           | CounterB[15:8] > last[7:0] |
| 78           | CounterB[15:8] = last[7:0] |
| 79           | CounterB[15:8] <= last[15:8] |
| 80           | CounterB[15:8] > last[15:8] |
| 81           | CounterB[15:8] = last[15:8] |
| 82           | CounterB[15:8] <= last[23:16] |
| 83           | CounterB[15:8] > last[23:16] |
| 84           | CounterB[15:8] = last[23:16] |
| 85           | CounterB[15:8] <= last[31:24] |
| 86           | CounterB[15:8] > last[31:24] |
| 87           | CounterB[15:8] = last[31:24] |
| 88           | CounterB[15:0] <= last[15:0] |
| 89           | CounterB[15:0] > last[15:0] |
| 90           | CounterB[15:0] = last[15:0] |
| 91           | CounterB[15:0] <= last[31:16] |
| 92           | CounterB[15:0] > last[31:16] |
| 93           | CounterB[15:0] = last[31:16] |
| 94           | Always 0 |
| 95           | Always 1 |
| 96-127       | The bits selected here are the same as the bits on the output register at the end of the previous cycle. |
```