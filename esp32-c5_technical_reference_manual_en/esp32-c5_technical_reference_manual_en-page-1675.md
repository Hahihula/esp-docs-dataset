

```markdown
Table 44.5-11. ADDCTI Opcode

ADDCTIc[H|L]
Add indirect (from most significant 16 bits of mux output) value to counter. Optionally only add to high or low 8 bits of counter.

Argument
c: Either A or B, indicate counter to use
h: If opcode is ADDCTIH, bit 24 to 31 of the output mux are added to the most significant 8 bits of the counter
l: If opcode is ADDCTILc, bit 16 to 23 of the output mux are added to the least significant 8 bits of the counter
If opcode is ADDCTIc, bit 16 to 31 of the output mux are added to all 16 bits of the counter (h=1, l=1)

Pseudo-code
if (h) begin
    ctr_c[15:8] <= ctr_c[15:8] + mux_out[31:24]
end else if (l) begin
    ctr_c[7:0] <= ctr_c[7:0] + mux_out[23:16]
end else begin
    ctr_c[15:0] <= ctr_c[15:0] + mux_out[31:16]
end
IP <= IP + 1

44.5.2 Configuration Registers

The BitScrambler is configured using a set of registers. Specifically, these registers are used to write a program into BitScrambler, write its LUT RAM, configure its behaviour, and start and stop BitScrambler operation. They are also used to attach a BitScrambler to a peripheral DMA path.

The ESP32-C5 only has one BitScrambler core which can either be placed in the TX path (where data is sent from the memory to a peripheral) or in a RX path (where data is sent from the peripheral to memory). For compatibility with other ESP series chips, when the BitScrambler core is placed in the TX path, it is controlled with the registers prefixed by BITSCRAMBLER_TX_ while when it is placed in the RX path, the registers prefixed by BITSCRAMBLER_RX_ govern its behaviour. Which path is active is decided by BITSCRAMBLER_RX_ENA and BITSCRAMBLER_TX_ENA, of which only one is allowed to be active at any given time.

Note:
For convenience, in this section we will refer to the TX path registers only; to get the RX path register descriptions, simply swap the prefixes.

When modifying the input or output of a peripheral, the BitScrambler needs to be attached to the DMA path of that peripheral. To do this, write the appropriate value for the peripheral into the HP_SYSTEM_BITSCRAMBLER_PERI_TX_SEL or HP_SYSTEM_BITSCRAMBLER_PERI_RX_SEL field of the HP_SYSTEM_BITSCRAMBLER_PERI_SEL_REG register.

The BitScrambler can also run in memory-to-memory mode. For this, the BITSCRAMBLER_LOOP_MODE bit in BITSCRAMBLER_SYS_REG needs to be set to one. In this mode, the TX BitScrambler is put into loopback mode while the RX BitScrambler is unused and unavailable. The BitScrambler still needs to be attached to a peripheral (although the peripheral does not need to be configured); the DMA path for this peripheral will be
```