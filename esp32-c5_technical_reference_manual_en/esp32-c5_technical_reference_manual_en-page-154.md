

```markdown
Chapter 3 RISC-V Trace Encoder (TRACE)

Register 3.11. TRACE_FILTER_CONTROL_REG (0x0028)
```

| Bit | Description |
|-----|-------------|
| 5   | TRACE_MATCH_INTERRUPT |
| 4   | TRACE_MATCH_ECAUSE |
| 3   | TRACE_MATCH_PRIVILEGE |
| 2   | TRACE_MATCH_COMP |
| 1   | TRACE_FILTER_EN |
| 0   | Reset |

TRACE_FILTER_EN Configure whether to enable filtering.
- 0: Disable
- 1: Enable
(R/W)

TRACE_MATCH_COMP Configures whether to enable the comparator match mode.
- 0: Disable
- 1: Enable
(R/W)

TRACE_MATCH_PRIVILEGE Configures whether to enable the privilege match mode.
- 0: Disable
- 1: Enable
(R/W)

TRACE_MATCH_ECAUSE Configures whether to enable the ecause match mode.
- 0: Disable
- 1: Enable
(R/W)

TRACE_MATCH_INTERRUPT Configures whether to enable the interrupt match mode.
- 0: Disable
- 1: Enable
(R/W)
```