

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE) GoBack


Register 2.11. TRACE_FILTER_CONTROL_REG (0x0028)


| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 5   | TRACE_FILTER_EN Configure whether to enable filtering.<br>0: Disable<br>1: Enable<br>(R/W) |
| 4   | TRACE_MATCH_COMP Configures whether to enable the comparator match mode.<br>0: Disable<br>1: Enable<br>(R/W) |
| 3   | TRACE_MATCH_PRIVILEGE Configures whether to enable the privilege match mode.<br>0: Disable<br>1: Enable<br>(R/W) |
| 2   | TRACE_MATCH_ECAUSE Configures whether to enable the ecause match mode.<br>0: Disable<br>1: Enable<br>(R/W) |
| 1   | TRACE_MATCH_INTERRUPT Configures whether to enable the interrupt match mode.<br>0: Disable<br>1: Enable<br>(R/W) |
| 0   | Reset |

Espressif Systems
Submit Documentation Feedback
ESP32-P4 TRM PRELIMINARY
```