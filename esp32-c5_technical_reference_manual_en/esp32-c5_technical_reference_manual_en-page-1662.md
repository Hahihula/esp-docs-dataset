

```markdown
Register 43.19. PARL_IO_TX_CLK_CFG_REG (0x0048)

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 | ... |   0 |

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
Register 43.20. PARL_IO_TX_CS_CFG_REG (0x004C)

| 31 | ... | 16 | 15 |
|----|-----|----|----|
| 0x00 |     |    | 0x00 |

PARL_IO_TX_CS_STOP_DELAY Configures the delay between the end of TX data transmission and the rising edge of TX_CS_O.
Unit: TX Core clock cycle
(R/W)

PARL_IO_TX_CS_START_DELAY Configures the delay between the falling edge of TX_CS_O and the start of TX data transmission.
Unit: TX Core clock cycle
(R/W)
```