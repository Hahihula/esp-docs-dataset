

```markdown
Register 15.38. TEE_CLOCK_GATE_REG (0x0080)

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | Reset |

TEE_CLK_EN Configures whether to keep the clock always on.
O: Enable automatic clock gating
1: Keep the clock always on
(R/W)
```

```markdown
Register 15.39. TEE_DATE_REG (0x0FFC)

| Bit 31 | 28 | 27 | ... | 0 |
|--------|----|----|-----|---|
|        |    |    |     | Reset |

0   0   0   Ox2205282

TEE_DATE_REG Version control register (R/W)
```