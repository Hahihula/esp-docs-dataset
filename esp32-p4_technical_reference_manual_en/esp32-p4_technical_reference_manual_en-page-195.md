

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE) GoBack

Register 2.9. TRACE_TRIGGER_REG (0x0020)

31 | 4 | 3 | 2 | 1 | 0
--+---+---+---+---+---
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 Reset

TRACE_TRIGGER_ON Configures whether to enable the encoder.
O: Invalid
1: Enable
(WT)

TRACE_TRIGGER_OFF Configures whether to disable the encoder.
O: Invalid
1: Disable
(WT)

TRACE_MEM_LOOP Configures the memory writing mode.
O: Non-loop mode
1: Loop mode
(R/W)

TRACE_RESTART_ENA Configures whether to enable automatic restart.
O: Disable
1: Enable
(R/W)
```