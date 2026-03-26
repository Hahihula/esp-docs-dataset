

```markdown
Register 54.18. SDHOST_BMOD_REG (0x0080)

31 | 11 | 10 | 8 | 7 | 6 | 2 | 1 | 0
--+-----+-----+----+---+---+---+---+---+
| O   |     |    |   |   |   |   |   | Reset

SDHOST_BMOD_SWR Configures whether to reset all DMA internal registers. It is automatically cleared after one clock cycle.
O: No effect
1: Reset
(R/W)

SDHOST_BMOD_FB Configures whether the AHB Master interface performs fixed burst transfers.
O: Use SINGLE and INCR burst transfer operations
1: Only use SINGLE, INCR4, INCR8 or INCR16 burst transfers
(R/W)

SDHOST_BMOD_DE Configures whether to enable the DMA.
O: Not enable
1: Enable
(R/W)

SDHOST_BMOD_PBL Configures the maximum number of beats to be performed in one DMA transaction.
0x0: 1-beat transfer
0x1: 4-beat transfer
0x2: 8-beat transfer
0x3: 16-beat transfer
0x4: 32-beat transfer
0x5: 64-beat transfer
0x6: 128-beat transfer
0x7: 256-beat transfer
(R/W)
```