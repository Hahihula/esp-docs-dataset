

```markdown
| ADDc[H|L] ctr_add |
|---|
| Add immediate value to counter indicated by c, and optionally write back only upper or lower 8 bits. |

| Argument | c: Either A or B, indicate counter to use<br/>ctr_add: 16-bit value to add to counter<br/>If opcode is ADDcH, only most significant 8 bits are written back<br/>If opcode is ADDcL, only least-significant 8 bits are written back<br/>If opcode is ADDc, all 16 bits will be written back (h=1, l=1). |
|---|
| Pseudo-code | tmp <= ctr_c + ctr_add<br/>if (h) begin<br/>    ctr_c[15:8] <= tmp[15:8]<br/>end<br/>if (l) begin<br/>    ctr_c[7:0] <= tmp[7:0]<br/>end<br/>IP <= IP + 1 |
| Note | The NOP (no operation) pseudo-op is encoded as ‘ADDA 0’. |

Table 59.4-6. ADD Opcode

IF ctl_cond_src, tgt
Jump to target if the indicated mux source bit is set.

| Argument | ctl_cond_src: Mux source (see CTR_MUX_SRC sources)<br/>tgt: 3-bit target instruction addresses |
|---|
| Pseudo-code | if (ctl_cond_src) begin<br/>    IP <= tgt<br/>end else begin<br/>    IP <= IP + 1<br/>end |
| Note | The JMP (always jump) pseudo-op is implemented as an ‘IF 95,tgt’ opcode, using the always-1 bit from the AUX bits. |

Table 59.4-7. IF Opcode

IFN ctl_cond_src, tgt
Jump to target if the indicated mux source bit is NOT set (note: same as IF but condition is negated).

| Argument | ctl_cond_src: Mux source (see CTR_MUX_SRC sources)<br/>tgt: 3-bit target instruction addresses |
|---|
| Pseudo-code | if (ctl_cond_src) begin<br/>    IP <= IP + 1<br/>end else begin<br/>    IP <= tgt<br/>end |
```