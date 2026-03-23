

```markdown
Register 34.14. SDIO_SLC1TX_LINK_REG (0x0054)

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    | (reserved) |   |
| Value | 1 | 0 | 0 | 0 |    |         | 0x0 Reset |

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

Register 34.15. SDIO_SLC1TX_LINK_ADDR_REG (0x0058)

```markdown
| Bit | 31 |
|-----|----|
|     |    |
| Value | 0x0 Reset |

SDIO_SLC1_TXLINK_ADDR Configures SLC1 TX linked list initial address. (R/W)
```

GoBack

Espressif Systems
1137
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```