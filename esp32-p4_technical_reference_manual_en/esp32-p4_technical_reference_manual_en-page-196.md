

```markdown
GoBack

Chapter 2 RISC-V Trace Encoder (TRACE)

Register 2.10. TRACE_CONFIG_REG (0x0024)
```

```plaintext
31                 6   5   4   3   2   1   0
+------------------+---+---+---+---+---+---+
|      (reserved)    | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
+------------------+---+---+---+---+---+---+---+
|                   Reset
```

```markdown
TRACE_DM_TRIGGER_ENA   Configure whether to enable the trigger signal.
    O: Disable
    1: Enable
    (R/W)

TRACE_RESET_ENA        Configures whether to enable the reset signal.
    O: Disable
    1: Enable
    (R/W)

TRACE_HALT_ENA         Configures whether to enable the halted signal.
    O: Disable
    1: Enable
    (R/W)

TRACE_STALL_ENA        Configures whether to enable the stall signal.
    O: Disable
    1: Enable
    (R/W)

TRACE_FULL_ADDRESS     Configure the address mode.
    O: Delta address mode
    1: Full address mode
    (R/W)
```