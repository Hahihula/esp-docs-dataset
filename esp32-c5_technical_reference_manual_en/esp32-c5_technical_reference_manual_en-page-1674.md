

```markdown
| LDCTDC[H|L] ctr_set                                                                 |
|--------------------------------------------------------------------------------------|
| Load counter direct (from immediate), and optionally only load high or low 8 bits of counter. |

Argument: c: Either A or B, indicate counter to use<br>ctr_set: 16-bit value to set the counter to<br>h: if opcode is LDCTDC h, only most significant 8 bits are set<br>l: if opcode is LDCTDCL, only least-significant 8 bits are set<br>If opcode is LDCTDC, all 16 bits are set (h=1, l=1)

Pseudo-code:
if (h) begin
    ctr_c[15:8] <= ctr_set[15:8]
end
if (l) begin
    ctr_c[7:0] <= ctr_set[7:0]
end
IP <= IP + 1

Table 44.5-9. LDCTD Opcode
```

```markdown
| LDICTIC[H|L]                                                                         |
|--------------------------------------------------------------------------------------|
| Load counter indirect (from most significant 16 bits of mux output), and optionally only load high or low 8 bits of counter. |

Argument: c: Either A or B, indicate counter to use<br>h: If opcode is LDICTIC h, only the most significant 8 bits are set<br>l: If opcode is LDICTICL, only the least significant 8 bits are set<br>If opcode is LDICTIC, all 16 bits are set (h=1, l=1)

Pseudo-code:
if (h) begin
    ctr_c[15:8] <= mux_out[31:24]
end
if (l) begin
    ctr_c[7:0] <= mux_out[23:16]
end
IP <= IP + 1

Table 44.5-10. LDICTI Opcode
```