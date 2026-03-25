

```markdown
Register 3.18. TRACE_CLOCK_GATE_REG (0x0044)

TRACE_CLK_EN Configures register clock gating.
- 0: Support clock only when the application writes registers to save power
- 1: Always force the clock on for registers
This bit doesn't affect register access (R/W)
```

```markdown
Register 3.19. TRACE_DATE_REG (0x03FC)

TRACE_DATE Version control register. (R/W)
```