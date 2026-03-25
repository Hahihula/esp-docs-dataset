

```markdown
Register 38.19. PARL_IO_TX_CLK_CFG_REG (0x0048)

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 | ... |   0 |

PARL_IO_TX_CLK_O_INV
PARL_IO_TX_CLK_I_INV

PARL_IO_TX_CLK_I_INV Configures whether to invert the TX input Core clock.
O: No effect
1: Invert
(R/W)

PARL_IO_TX_CLK_O_INV Configures whether to invert the TX output Core clock.
O: No effect
1: Invert
(R/W)
```

```markdown
Register 38.20. PARL_IO_CLK_REG (0x0120)

| 31 | 30 |
|----:|----:|
|   0 |   0 |

PARL_IO_CLK_EN

PARL_IO_CLK_EN Configures whether to force clock on for this register file.
O: No effect
1: Force clock on
(R/W)
```

```markdown
Register 38.21. PARL_IO_VERSION_REG (0x03FC)

| 31 | 28 | 27 |
|----:|----:|----:|
|   0 |   0 |   0 |

PARL_IO_DATE

PARL_IO_DATE Version control register. (R/W)
```

```markdown
Espressif Systems
1223
ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback
```