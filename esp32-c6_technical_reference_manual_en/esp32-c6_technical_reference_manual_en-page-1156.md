

```markdown
Register 34.43. SLCHOST_SLCOHOST_INT_ST_REG (0x0058)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | SLCHOST_SLCO_RX_NEW_PACKET_INT_ST | (reserved) | SLCHOST_SLCO_TX_OVF_INT_ST | SLCHOST_SLCO_TOHOST_BITn_INT_ST | (reserved) | Reset |
| Value | 0x0 | 0 | 0xD | 0 | 0 | 0xD | 0 |    |

SLCHOST_SLCO_TOHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLCHOST_SLCO_TOHOST_BITn_INT. (n: 0-7). (RO)

SLCHOST_SLCO_RX_UDF_INT_ST The masked interrupt status of SLCHOST_SLCO_RX_UDF_INT. (RO)

SLCHOST_SLCO_TX_OVF_INT_ST The masked interrupt status of SLCHOST_SLCO_TX_OVF_INT. (RO)

SLCHOST_SLCO_RX_NEW_PACKET_INT_ST The masked interrupt status of SLCHOST_SLCO_RX_NEW_PACKET_INT. (RO)
```