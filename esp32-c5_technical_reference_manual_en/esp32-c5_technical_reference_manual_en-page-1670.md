

```markdown
- CTL_MUX_REL, CTL_CTR_SRC_SEL and CTR_LUT_SRC_SEL: Select which bits are available to select using the CTL_MUX_SEL bits.
  - CTRL_CTR_SRC_SEL (Control Counter Source Select) makes the bits from counter A and B available
  - CTL_LUT_SRC_SEL (Control LUT Source Select) makes the output value of the LUT RAM available. See Table 44.5-3 for details.
  - When CTL_MUX_REL (Control Mux Relative) is 1, the BitScrambler applies the value of counter A as an offset to any CTL_MUX_SEL_n value that is 63 or below. The exact behaviour depends on CTR_SRC_SEL, as detailed in Table 44.5-2.

Table 44.5-2. Effective CTL_MUX_SEL_n values when CTL_MUX_REL is 1

| Condition                                                                 | Effective value of CTL_MUX_SEL |
|---------------------------------------------------------------------------|-------------------------------|
| CTL_MUX_SEL_n >= 64                                                      | CTL_MUX_SEL (unchanged)       |
| CTL_MUX_SEL_n < 64 and CTL_CTR_SRC_SEL = 0                                | (CTL_MUX_SEL_n + CTRA) & 63    |
| CTL_MUX_SEL_n < 31 and CTL_CTR_SRC_SEL = 1                                | (CTL_MUX_SEL_n + CTRA) & 31    |
| 32 <= CTL_MUX_SEL_n < 64 and CTL_CTR_SRC_SEL = 1                         | ((CTL_MUX_SEL_n + CTRA) & 31) + 32 |

Of these fields, most are data path configuration items. The field that affects the control path is OPCODE, although CTL_MUX_REL, CTL_CTR_SRC_SEL, and CTR_LUT_SRC_SEL may influence how some of the opcodes work by adjusting the source selection for the IF/IFN opcodes.

CTL_MUX_SEL_n: These fields, one for each bit in the output register, select the source for that particular bit. The specific bit chosen is partially dependent on the settings of the CTL_MUX_REL, CTL_CTR_SRC_SEL, and CTR_LUT_SRC_SEL. Given CTL_MUX_SRC_n has value N, the bit is selected as described in Table 44.5-3. Note that the source selection for IF/IFN opcodes is affected in the same way.

Table 44.5-3. CTL_MUX_SEL Values

| Bit | Description |
|-----|-------------|
| 0-31 | The bit is sourced from bit N in the incoming FIFO register. |
|     | The source of the bit depends on the setting of CTL_CTR_SRC_SEL and CTR_LUT_SRC_SEL: <br> If CTL_CTR_SRC_SEL = 0: the bit is sourced from bit N in the incoming FIFO register. <br> If CTL_CTR_SRC_SEL = 1: the bit is sourced from bit (N-32) of the counter registers. Specifically, if N is 32 to 47, the bit is sourced from bit (N-32) of counter A and if N is 48 to 63, the bit is sourced from bit (N-48) of counter B. <br> If CTL_LUT_SRC_SEL = 1: Depending on the width of the LUT (8, 16, or 32 bits), a read of the top 8, 16, or 32 bits will return data from the LUT rather than what CTL_CTR_SRC_SEL selects. Specifically, given a LUT width of N, 63 will return LUT output bit (N-1), 62 will return LUT output bit (N-2) and so on. |
| 64 | CounterB[7:0] <= last[7:0] |
| 65 | CounterB[7:0] > last[7:0] |
| 66 | CounterB[7:0] = last[7:0] |
| 67 | CounterB[7:0] <= last[15:8] |
| 68 | CounterB[7:0] > last[15:8] |
| 69 | CounterB[7:0] = last[15:8] |
```