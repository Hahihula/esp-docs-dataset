

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE) GoBack

Register 2.11. TRACE_FILTER_CONTROL_REG (0x0028)

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 5   | TRACE_FILTER_EN |
| 4   | TRACE_MATCH_COMP |
| 3   | TRACE_MATCH_PRIVILEGE |
| 2   | TRACE_MATCH_ECAUSE |
| 1   | TRACE_MATCH_INTERRUPT |
| 0   | Reset       |

TRACE_FILTER_EN Configure whether to enable filtering.
O: Disable
1: Enable
(R/W)

TRACE_MATCH_COMP Configures whether to enable the comparator match mode.
O: Disable
1: Enable
(R/W)

TRACE_MATCH_PRIVILEGE Configures whether to enable the privilege match mode.
O: Disable
1: Enable
(R/W)

TRACE_MATCH_ECAUSE Configures whether to enable the ecause match mode.
O: Disable
1: Enable
(R/W)

TRACE_MATCH_INTERRUPT Configures whether to enable the interrupt match mode.
O: Disable
1: Enable
(R/W)
```