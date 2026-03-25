

```markdown
Register 30.8. SDIO_SLCORX_LINK_REG (0x003C)

| 31 | 30 | 29 | 28 | 27 | [reserved] |
|----:|----:|----:|----:|----:|------------|
|   1 |   0 |   0 |   0 |    |            |

SDIO_SLCO_RXLINK_STOP Configures whether to stop SLCO RX linked list operation.
- O: No effect
- 1: Stop the operation (R/W/SC)

SDIO_SLCO_RXLINK_START Configures whether to start SLCO RX linked list operation from the address indicated by SDIO_SLCO_RXLINK_ADDR.
- O: No effect
- 1: Start the operation (R/W/SC)

SDIO_SLCO_RXLINK_RESTART Configures whether to restart and continue SLCO RX linked list operation.
- O: No effect
- 1: Restart the operation (R/W/SC)

SDIO_SLCO_RXLINK_PARK Represents SLCO RX linked list FSM state.
- O: The FSM not in idle state
- 1: The FSM in idle state (RO)
```

Register 30.9. SDIO_SLCORX_LINK_ADDR_REG (0x0040)

```markdown
| 31 | [reserved] |
|----|------------|
|   |            |

SDIO_SLCO_RXLINK_ADDR Configures SLCO RX linked list initial address. (R/W)
```

Espressif Systems

Submit Documentation Feedback PRELIMINARY