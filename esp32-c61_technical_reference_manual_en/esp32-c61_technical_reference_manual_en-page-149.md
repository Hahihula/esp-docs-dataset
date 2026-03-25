

```markdown
Chapter 2 RISC-V Trace Encoder (TRACE)

Register 2.12. TRACE_FILTER_MATCH_CONTROL_REG (0x002C)
```

```plaintext
31                                 7 6                                  2 1 0
+-------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+-------------------------------------------------------------------------------------------------+
```

```markdown
TRACE_MATCH_CHOICE_PRIVILEGE Configures the privilege level for matching.
    0: User mode
    1: Machine mode
    (R/W)

TRACE_MATCH_VALUE_INTERRUPT Configures the interrupt level for matching. Valid only when TRACE_MATCH_INTERRUPT is set.
    0: itype=1
    1: itype=2
    (R/W)

TRACE_MATCH_CHOICE_ECAUSE Configures the ecause code for matching. (R/W)
```