

```markdown
| Bit       | Field                  | Bit       | Field               |
|-----------|------------------------|-----------|---------------------|
| 0 - 6     | CTL_MUX_SEL_0          | 133 - 139 | CTL_MUX_SEL_19      |
| 7 - 13    | CTL_MUX_SEL_1          | 140 - 146 | CTL_MUX_SEL_20      |
| 14 - 20   | CTL_MUX_SEL_2          | 147 - 153 | CTL_MUX_SEL_21      |
| 21 - 27   | CTL_MUX_SEL_3          | 154 - 160 | CTL_MUX_SEL_22      |
| 28 - 34   | CTL_MUX_SEL_4          | 161 - 167 | CTL_MUX_SEL_23      |
| 35 - 41   | CTL_MUX_SEL_5          | 168 - 174 | CTL_MUX_SEL_24      |
| 42 - 48   | CTL_MUX_SEL_6          | 175 - 181 | CTL_MUX_SEL_25      |
| 49 - 55   | CTL_MUX_SEL_7          | 182 - 188 | CTL_MUX_SEL_26      |
| 56 - 62   | CTL_MUX_SEL_8          | 189 - 195 | CTL_MUX_SEL_27      |
| 63 - 69   | CTL_MUX_SEL_9          | 196 - 202 | CTL_MUX_SEL_28      |
| 70 - 76   | CTL_MUX_SEL_10         | 203 - 209 | CTL_MUX_SEL_29      |
| 77 - 83   | CTL_MUX_SEL_11         | 210 - 216 | CTL_MUX_SEL_30      |
| 84 - 90   | CTL_MUX_SEL_12         | 217 - 223 | CTL_MUX_SEL_31      |
| 91 - 97   | CTL_MUX_SEL_13         | 224 - 249 | OPCODE              |
| 98 - 104  | CTL_MUX_SEL_14         | 250 - 251 | CTL_READ_IN         |
| 105 - 111 | CTL_MUX_SEL_15         | 252 - 253 | CTL_WR_OUT          |
| 112 - 118 | CTL_MUX_SEL_16         | 254       | CTL_MUX_REL         |
| 119 - 125 | CTL_MUX_SEL_17         | 255       | CTL_CTR_SRC_SEL     |
| 126 - 132 | CTL_MUX_SEL_18         | 256       | CTL_LUT_SRC_SEL     |

The meanings of these fields are as follows:

*   `CTL_MUX_SEL_n`: This 7-bit field selects the source of bit n in the output register. See Table 44.5-3 for details.
*   `OPCODE`: These bits encode an opcode. For the bit pattern of this field, please refer to Table 44.5-4.
*   `CTL_READ_IN`: This selects the number of bits that are read from the input FIFO at the end of the instruction:

    -   0: Do not read any data
    -   1: Read 8 bits
    -   2: Read 16 bits
    -   3: Read 32 bits

*   `CTL_WR_OUT`: This selects the number of bits that are written from the output register to the output FIFO at the end of the instruction:

    -   0: Do not write any data
    -   1: Write 8 bits
    -   2: Write 16 bits
    -   3: Write 32 bits
```