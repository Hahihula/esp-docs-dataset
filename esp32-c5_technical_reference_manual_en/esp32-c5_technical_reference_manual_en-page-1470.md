

```markdown
Register 39.10. SDIO_SLCOTX_LINK_REG (0x0044)

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    | (reserved) |   |
| Value | 1 | 0 | 0 |    |    |         | Reset |

SDIO_SLCO_TXLINK_STOP Configures whether to stop SLCO TX linked list operation.
- 0: No effect
- 1: Stop the operation (R/W/SC)

SDIO_SLCO_TXLINK_START Configures whether to start SLCO TX linked list operation from the address indicated by SDIO_SLCO_TXLINK_ADDR.
- 0: No effect
- 1: Start the operation (R/W/SC)

SDIO_SLCO_TXLINK_RESTART Configures whether to restart and continue SLCO TX linked list operation.
- 0: No effect
- 1: Restart the operation (R/W/SC)

SDIO_SLCO_TXLINK_PARK Represents SLCO TX linked list FSM state.
- 0: The FSM not in idle state
- 1: The FSM in idle state (RO)
```

Register 39.11. SDIO_SLCOTX_LINK_ADDR_REG (0x0048)

```markdown
| Bit | 31 |
|-----|----|
|     |    |
| Value | 0x0 |
| Reset |    |

SDIO_SLCO_TXLINK_ADDR Configures SLCO TX linked list initial address. (R/W)
```