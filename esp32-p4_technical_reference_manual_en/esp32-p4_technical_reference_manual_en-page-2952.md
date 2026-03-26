

```markdown
Table 59.4-9. LDCTD Opcode

| LDCTDc[H|L] ctr_set                                                                 |
|--------------------------------------------------------------------------------------|
| Load counter direct (from immediate), and optionally only load high or low 8 bits of counter. |

Argument | c: Either A or B, indicate counter to use<br>ctr_set: 16-bit value to set the counter to<br>h: if opcode is LDCTDcH, only most significant 8 bits are set<br>l: if opcode is LDCTDcL, only least-significant 8 bits are set<br>If opcode is LDCTDc, all 16 bits are set (h=1, l=1) |
|---|---|
| Pseudo-code | if (h) begin<br>    ctr_c[15:8] <= ctr_set[15:8]<br>end<br>if (l) begin<br>    ctr_c[7:0] <= ctr_set[7:0]<br>end<br>IP <= IP + 1 |

Table 59.4-10. LDCTI Opcode

| LDCTIc[H|L]                                                                 |
|------------------------------------------------------------------------------|
| Load counter indirect (from most significant 16 bits of mux output), and optionally only load high or low 8 bits of counter. |

Argument | c: Either A or B, indicate counter to use<br>h: If opcode is LDCTIcH, only the most significant 8 bits are set<br>l: If opcode is LDCTIcL, only the least significant 8 bits are set<br>If opcode is LDCTIc, all 16 bits are set (h=1, l=1) |
|---|---|
| Pseudo-code | if (h) begin<br>    ctr_c[15:8] <= mux_out[31:24]<br>end<br>if (l) begin<br>    ctr_c[7:0] <= mux_out[23:16]<br>end<br>IP <= IP + 1 |
```

## 59.4.2 Configuration Registers

The BitScrambler is configured using a set of registers. Specifically, these registers are used to write a program into BitScrambler, write its LUT RAM, configure its behaviour, and start and stop BitScrambler operation. They are also used to attach a BitScrambler to a peripheral DMA path.

The ESP32-P4 has two BitScramblers: one can be placed in the TX path (where data is sent from the memory to a peripheral) while the other can be placed in a RX path (where data is sent from the peripheral to memory). The configuration registers for the two BitScramblers are the same, with the only difference being the TX path BitScrambler registers are prefixed by BITSCRAMBLER_TX_ while the RX path BitScrambler uses BITSCRAMBLER_RX_ prefixes.
```