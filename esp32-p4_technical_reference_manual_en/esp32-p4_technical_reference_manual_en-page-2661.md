

```markdown
Register 52.25. EMACLPI_CSR_REG (0x0030)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    | (reserved) | LPITXA | PLS | LPIEN | (reserved) | RLPIST | TLPIST | (reserved) | RLPIEX | RLPIEN | TLPIEN |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

LPITXA Configures the behavior of the MAC when it is entering or coming out of the LPI mode on the transmit side.
O: This bit directly controls behavior of the MAC when it is entering or coming out of the LPI mode.
1: This bit controls behavior of the MAC when it is entering or coming out of the LPI mode in combination with LPIEN. When LPIEN is also 1, the MAC enters the LPI mode only after all outstanding frames (in the core) and pending frames (in the application interface) have been transmitted. The MAC comes out of the LPI mode when the application sends any frame for transmission
(R/W)

PLS Configures the link status of the PHY.
O: Link up
1: Link down
(R/W)

LPIEN Configures whether the EMAC transmitter enters the LPI state.
O: Exit
1: Enter
This bit is cleared when the LPITXA bit is set and the MAC exits the LPI state because of the arrival of a new packet for transmission.
(R/W/SC)

RLPIST Represents the receive LPI state.
O: Inactive
1: The EMAC is receiving the LPI pattern
(RO)

TLPIST Represents the transmit LPI state.
O: Inactive
1: The EMAC is transmitting the LPI pattern
(RO)

RLPIEX Represents the receive LPI exit state.
O: Inactive
1: The EMAC Receiver has stopped receiving the LPI pattern, exited the LPI state, and resumed the normal reception
(R/SS/RC)
```
Continued on the next page...
```