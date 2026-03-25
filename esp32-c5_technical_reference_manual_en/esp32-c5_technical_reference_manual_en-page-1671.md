

```markdown
| Bit | Description |
|-----|-------------|
| 70  | CounterB[7:0] <= last[23:16] |
| 71  | CounterB[7:0] > last[23:16] |
| 72  | CounterB[7:0] = last[23:16] |
| 73  | CounterB[7:0] <= last[31:24] |
| 74  | CounterB[7:0] > last[31:24] |
| 75  | CounterB[7:0] = last[31:24] |
| 76  | CounterB[15:8] <= last[7:0] |
| 77  | CounterB[15:8] > last[7:0] |
| 78  | CounterB[15:8] = last[7:0] |
| 79  | CounterB[15:8] <= last[15:8] |
| 80  | CounterB[15:8] > last[15:8] |
| 81  | CounterB[15:8] = last[15:8] |
| 82  | CounterB[15:8] <= last[23:16] |
| 83  | CounterB[15:8] > last[23:16] |
| 84  | CounterB[15:8] = last[23:16] |
| 85  | CounterB[15:8] <= last[31:24] |
| 86  | CounterB[15:8] > last[31:24] |
| 87  | CounterB[15:8] = last[31:24] |
| 88  | CounterB[15:0] <= last[15:0] |
| 89  | CounterB[15:0] > last[15:0] |
| 90  | CounterB[15:0] = last[15:0] |
| 91  | CounterB[15:0] <= last[31:16] |
| 92  | CounterB[15:0] > last[31:16] |
| 93  | CounterB[15:0] = last[31:16] |
| 94  | Always 0 |
| 95  | Always 1 |
| 96-127 | The bits selected here are the same as the bits on the output register at the end of the previous cycle. |

The BitScrambler recognizes seven opcodes, which are encoded in the opcode fields as shown in Table 44.5-4.

Table 44.5-4. Instruction Opcode
| Opcode | Bit 25 | Bit 24 | Bit 23 | Bit 22 | Bit 21 | Bit 20 | Bit 19 | Bit 18 | Bit 17 | Bit 16 | Bit 15 | Bit 14 | Bit 13 | Bit 12 | Bit 11 | Bit 10 | Bit 9 | Bit 8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| LOOP   | 1      | c      |        | tgt    |        |        |        |        |        | end_val|        |        |        |        |        |        |        | ctr_add|        |        |        |        |        |        |        |        |
| ADD    | O      | c      | h      | I      | 0      | 0      | 0      | 0      | 0      |        |        |        |        |        |        |        |        | ctr_add|        |        |        |        |        |        |        |        |
| IF     | O      | O      |        | tgt    |        | 0      | 0      | 0      | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | src    |        |        |        |        |        |        |        |        |
| IFN    | O      | O      |        | tgt    |        | 0      | 0      | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | src    |        |        |        |        |        |        |        |        |
| LDCTD  | O      | c      | h      | I      | 0      | 0      | 0      | 1      | 1      |        |        |        |        |        |        |        | ctr_set|        |        |        |        |        |        |        |        |        |
| LDCTI  | O      | c      | h      | I      | 0      | 0      | 0      | 1      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      | 0      |        |        |        |        |        |        |        |        |        |
| ADDCTI | O      | c      | h      | I      | 0      | 0      | 0      | 1      | 0      | 0      | 1      | 0      | 0      | 0      | 0      | 0      | 0      |        |        |        |        |        |        |        |        |        |

The fields are defined as follows:
```