

```markdown
Register 30.14. SDIO_SLC1TX_LINK_REG (0x0054)

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    | SDIO_SLC1_TXLINK_PARK | SDIO_SLC1_TXLINK_RESTART | SDIO_SLC1_TXLINK_START | SDIO_SLC1_TXLINK_STOP | (reserved) | 0 |
| Value | 1 | 0 | 0 | 0 | ... | ... | 0x0 |
| Reset |    |    |    |    |     |     | Reset |

SDIO_SLC1_TXLINK_STOP Configures whether to stop SLC1 TX linked list operation.
- 0: No effect
- 1: Stop the operation (R/W/SC)

SDIO_SLC1_TXLINK_START Configures whether to start SLC1 TX linked list operation from the address indicated by SDIO_SLC1_TXLINK_ADDR.
- 0: No effect
- 1: Start the operation (R/W/SC)

SDIO_SLC1_TXLINK_RESTART Configures whether to restart and continue SLC1 TX linked list operation.
- 0: No effect
- 1: Restart the operation (R/W/SC)

SDIO_SLC1_TXLINK_PARK Represents SLC1 TX linked list FSM state.
- 0: The FSM not in idle state
- 1: The FSM in idle state (RO)
```

Register 30.15. SDIO_SLC1TX_LINK_ADDR_REG (0x0058)

```markdown
| Bit | 31 |
|-----|----|
|     |    |
| Value | 0x0 |
| Reset | Reset |

SDIO_SLC1_TXLINK_ADDR Configures SLC1 TX linked list initial address. (R/W)
```

Espressif Systems

Submit Documentation Feedback

ESP32-C61 TRM (Pre-release v0.5)

PRELIMINARY
```