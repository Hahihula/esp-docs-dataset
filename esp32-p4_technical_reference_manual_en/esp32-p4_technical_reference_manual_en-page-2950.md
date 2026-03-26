

```markdown
| Bit | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|---|
| LOOP | 1 | c | tgt |    |    |    |    |    |    |    |    |    |    |    |    |    |    | end_val | ctr_add |
| ADD   | 0 | c | h | I | O | 0 | 0 | 0 | 0 | 0 |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
| IF     | 0 | 0 |    | tgt | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | src |
| IFN    | 0 | 0 |    | tgt | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |    |    | src |
| LDCTD  | 0 | c | h | I | O | 0 | 0 | 0 | 1 | 1 |    |    |    |    |    | ctr_set |    |    |    |    |    |    |    |    |    |    |
| LDCTI  | 0 | c | h | I | O | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |    |    |
```

The fields are defined as follows:

*   c: Configures which counter to use.
    -  0: counter A
    -  1: counter B
*   end_val, ctr_add, ctr_set: 16-bit (or 5-bit) value. Please refer to the instruction descriptions below for the meanings of these fields.
*   tgt: The location of an instruction. Range: 0 ~ 7.
*   h: 1 if the upper 8 bits need to be written back to a counter.
*   I: 1 if the lower 8 bits need to be written back to a counter.

Note that if an opcode does not specify H or L, it is assumed that the full 16 bits need to be written back and the h and I bits will both be 1.

These six opcodes affect the state of the BitScrambler as follows:

Table 59.4-5. LOOP Opcode

| LOOPc end_val, ctr_add, tgt | Loop on counter indicated by c, add ctr_add to the counter, and loop back to tgt until the counter reaches end_val. When that happens, reset the counter and fall through. |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument                    | c: Either A or B, indicates counter to use<br>tgt: 3-bit target instruction addresses<br>end_val: 16-bit value to compare the counter to<br>ctr_add: 5-bit signed value to add to the counter |
| Pseudo-code                 | if ((unsigned)ctrC < end_val) begin<br>&nbsp;&nbsp;IP <= tgt<br>&nbsp;&nbsp;ctr_c <= ctr_c + sign_extend(ctr_add)<br>end else begin<br>&nbsp;&nbsp;IP <= IP + 1<br>&nbsp;&nbsp;ctr_c <= 0<br>end |