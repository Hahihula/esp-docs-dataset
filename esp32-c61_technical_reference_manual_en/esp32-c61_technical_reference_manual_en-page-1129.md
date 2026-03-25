

```markdown
Register 30.10. SDIO_SLCOTX_LINK_REG (0x0044)

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    | SDIO_SLCOTX_LINK_PARK | SDIO_SLCOTX_LINK_RESTART | SDIO_SLCOTX_LINK_START | SDIO_SLCOTX_LINK_STOP | (reserved) | 0 |
| Value at Reset | 1 | 0 | 0 | ... | ... | ... | 0 |

SDIO_SLCOTX_LINK_STOP Configures whether to stop SLCO TX linked list operation.
- 0: No effect
- 1: Stop the operation (R/W/SC)

SDIO_SLCOTX_LINK_START Configures whether to start SLCO TX linked list operation from the address indicated by SDIO_SLCOTX_LINK_ADDR.
- 0: No effect
- 1: Start the operation (R/W/SC)

SDIO_SLCOTX_LINK_RESTART Configures whether to restart and continue SLCO TX linked list operation.
- 0: No effect
- 1: Restart the operation (R/W/SC)

SDIO_SLCOTX_LINK_PARK Represents SLCO TX linked list FSM state.
- 0: The FSM not in idle state
- 1: The FSM in idle state (RO)
```

Register 30.11. SDIO_SLCOTX_LINK_ADDR_REG (0x0048)

```markdown
| Bit | 31 |
|-----|----|
|     |    |

Value at Reset:
| Bit | 0x0 | Reset |
|-----|-----|-------|

SDIO_SLCOTX_LINK_ADDR Configures SLCO TX linked list initial address. (R/W)
```

GoBack
```