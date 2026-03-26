

```markdown
- OPCODE: These bits encode an opcode. For the bit pattern of this field, please refer to Table 59.4-4.
- CTL_READ_IN: This selects the number of bits that are read from the input FIFO at the end of the instruction:
    - 0: Do not read any data
    - 1: Read 8 bits
    - 2: Read 16 bits
    - 3: Read 32 bits
- CTL_WR_OUT: This selects the number of bits that are written from the output register to the output FIFO at the end of the instruction:
    - 0: Do not write any data
    - 1: Write 8 bits
    - 2: Write 16 bits
    - 3: Write 32 bits
- CTL_MUX_REL, CTL_CTR_SRC_SEL and CTR_LUT_SRC_SEL: Select which bits are available to select using the CTL_MUX_SEL bits.
    - CTRL_CTR_SRC_SEL (Control Counter Source Select) makes the bits from counter A and B available
    - CTL_LUT_SRC_SEL (Control LUT Source Select) makes the output value of the LUT RAM available. See Table 59.4-3 for details.
- When CTL_MUX_REL (Control Mux Relative) is 1, the BitScrambler applies the value of counter A as an offset to any CTL_MUX_SEL_n value that is 63 or below. The exact behaviour depends on CTR_SRC_SEL, as detailed in Table 59.4-2.
```

**Table 59.4-2. Effective CTL_MUX_SEL_n values when CTL_MUX_REL is 1**

| Condition | Effective value of CTL_MUX_SEL |
|-----------|-------------------------------|
| CTL_MUX_SEL_n >= 64 | CTL_MUX_SEL (unchanged) |
| CTL_MUX_SEL_n < 64 and CTL_CTR_SRC_SEL = 0 | (CTL_MUX_SEL_n + CTRA) & 63 |
| CTL_MUX_SEL_n < 31 and CTL_CTR_SRC_SEL = 1 | (CTL_MUX_SEL_n + CTRA) & 31 |
| 32 <= CTL_MUX_SEL_n < 64 and CTL_CTR_SRC_SEL = 1 | ((CTL_MUX_SEL_n + CTRA) & 31) + 32 |

Of these fields, most are data path configuration items. The field that affects the control path is OPCODE, although CTL_MUX_REL, CTL_CTR_SRC_SEL, and CTR_LUT_SRC_SEL may influence how some of the opcodes work by adjusting the source selection for the IF/IFN opcodes.

CTL_MUX_SEL_n: These fields, one for each bit in the output register, select the source for that particular bit. The specific bit chosen is partially dependent on the settings of the CTL_MUX_REL, CTL_CTR_SRC_SEL and CTR_LUT_SRC_SEL. Given CTL_MUX_SRC_n has value N, the bit is selected as described in Table 59.4-3. Note that the source selection for IF/IFN opcodes is affected in the same way.
```