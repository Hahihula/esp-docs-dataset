

```markdown
## Register 34.10. SDIO_SLCOTX_LINK_REG (0x0044)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | SDIO_SLCO_TXLINK_PARK                                                       |
| 30  | SDIO_SLCO_TXLINK_RESTART                                                   |
| 29  | SDIO_SLCO_TXLINK_START                                                     |
| 28  | SDIO_SLCO_TXLINK_STOP                                                      |
|     | (reserved)                                                                 |
| 27  | Reset                                                                      |

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

## Register 34.11. SDIO_SLCOTX_LINK_ADDR_REG (0x0048)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | SDIO_SLCO_TXLINK_ADDR                                                      |
|     | Reset                                                                      |

SDIO_SLCO_TXLINK_ADDR Configures SLCO TX linked list initial address. (R/W)
```