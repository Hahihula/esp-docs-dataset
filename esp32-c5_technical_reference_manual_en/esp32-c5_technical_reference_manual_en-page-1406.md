

```markdown
Register 38.3. TWAIFD_COMMAND_REG (0x000C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 11  | reserved                                                                     |
| 10  | TWAIFD_CTXYPE                                                                |
| 9   | TWAIFD_TXCRSTE                                                              |
| 8   | TWAIFD_RXFCRST                                                              |
| 7   | TWAIFD_ERCRST                                                               |
| 6   | TWAIFD_CDO                                                                  |
| 5   | TWAIFD_RRB                                                                   |
| 4   | TWAIFD_RXRPVM                                                                |
| 3-0 | reserved                                                                    |

TWAIFD_RXRPVM Configures whether to move RX buffer read pointer forward.
O: No action
1: Move forward
(WO)

TWAIFD_RRB Configures whether to flush the RX buffer and reset its memory pointers.
O: Invalid
1: Flush
(WO)

TWAIFD_CDO Configures whether to clear the data overrun flag in the RX buffer.
O: Invalid
1: Clear
(WO)

TWAIFD_ERCRST Configures whether to reset error counters. When CAN FD is not bus-off, or is bus-off due to being disabled (TWAIFD_ENA = 0), this command has no effect.
O: Invalid
1: Reset
(WO)

TWAIFD_RXFCRST Configures whether to clear the RX bus traffic counter RX_COUNTER.
O: Invalid
1: Clear
(WO)

TWAIFD_TXFCRST Configures whether to clear the TX bus traffic counter TX_COUNTER.
O: Invalid
1: Clear
(WO)

TWAIFD_CPEXS Configures whether to clear the protocol exception flag.
O: Invalid
1: Clear
(WO)
```