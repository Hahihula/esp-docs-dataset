

```markdown
Register 39.12. SDIO_SLC1RX_LINK_REG (0x004C)

SDIO_SLC1_RXLINK_STOP Configures whether to stop SLC1 RX linked list operation.
- 0: No effect
- 1: Stop the operation (R/W/SC)

SDIO_SLC1_RXLINK_START Configures whether to start SLC1 RX linked list operation from the address indicated by SDIO_SLC1_RXLINK_ADDR.
- 0: No effect
- 1: Start the operation (R/W/SC)

SDIO_SLC1_RXLINK_RESTART Configures whether to restart and continue SLC1 RX linked list operation.
- 0: No effect
- 1: Restart the operation (R/W/SC)

SDIO_SLC1_RXLINK_PARK Represents SLC1 RX linked list FSM state.
- 0: The FSM not in idle state
- 1: The FSM in idle state (RO)
```

```markdown
Register 39.13. SDIO_SLC1RX_LINK_ADDR_REG (0x0050)

SDIO_SLC1_RXLINK_ADDR Configures SLC1 RX linked list initial address. (R/W)
```