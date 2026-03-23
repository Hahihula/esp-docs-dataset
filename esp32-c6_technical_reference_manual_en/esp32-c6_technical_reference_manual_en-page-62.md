

```markdown
Register 1.25. MSIP (0x1800)

MSIP Configures the pending status of the machine software interrupt.
O: Not pending
1: Pending
(R/W)
```

```markdown
Register 1.26. MTIMECTL (0x1804)

MTCE Configures whether to enable the CLINT timer counter.
O: Not enable
1: Enable
(R/W)

MTIE Write 1 to enable the machine timer interrupt. (R/W)

MTIP Represents the pending status of the machine timer interrupt.
O: Not pending
1: Pending
(RO)

MTOF Configures whether the machine timer overflows.
O: Not overflow
1: Overflow
(R/W)
```