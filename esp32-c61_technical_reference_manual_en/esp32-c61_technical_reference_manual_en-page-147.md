

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE) GoBack


Register 2.10. TRACE_CONFIG_REG (0x0024)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 7   | TRACE_FULL_ADDRESS          | Configure the address mode.<br>0: Delta address mode<br>1: Full address mode |
| 4   | TRACE_STALL_ENA             | Configures whether to enable the stall signal.<br>0: Disable<br>1: Enable (R/W)|
| 3   | TRACE_HALT_ENA              | Configures whether to enable the halted signal.<br>0: Disable<br>1: Enable (R/W)|
| 2   | TRACE_RESET_ENA             | Configures whether to enable the reset signal.<br>0: Disable<br>1: Enable (R/W)|
| 1   | TRACE_DM_TRIGGER_ENA        | Configure whether to enable the trigger signal.<br>0: Disable<br>1: Enable (R/W)|
| 0   |                             | Reset                                                                       |
```