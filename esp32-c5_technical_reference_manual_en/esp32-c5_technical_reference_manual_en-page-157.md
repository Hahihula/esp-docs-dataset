

```markdown
Chapter 3 RISC-V Trace Encoder (TRACE)

Register 3.13. TRACE_FILTER_COMPARATOR_CONTROL_REG (0x0030)

Continued from the previous page...

TRACE_S_NOTIFY Configures whether to explicitly report an instruction address matched against the secondary comparator.
O: Not report
1: Report
(R/W)

TRACE_MATCH_MODE Configures the comparator match condition.
O: Only the primary comparator matches
1: Both primary and secondary comparators match (P&S)
2: Neither primary nor secondary comparator match (!P&S)
3: Start filtering when the primary comparator matches and stop filtering when the secondary comparator matches
(R/W)

Register 3.14. TRACE_FILTER_P_COMPARATOR_MATCH_REG (0x0034)

TRACE_P_MATCH Configures the match value for the primary comparator. (R/W)

Register 3.15. TRACE_FILTER_S_COMPARATOR_MATCH_REG (0x0038)

TRACE_S_MATCH Configures the match value for the secondary comparator. (R/W)
```