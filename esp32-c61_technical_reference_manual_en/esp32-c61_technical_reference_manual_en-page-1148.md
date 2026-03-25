

```markdown
Register 30.41. SLCHOST_SLCOHOST_INT_RAW_REG (0x0050)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | SLCHOST_SLCO_RX_NEW_PACKET_INT_RAW | (reserved) | SLCHOST_SLCO_TX_OVF_INT_RAW | (reserved) | SLCHOST_SLCO_TOHOST_BITn_INT_RAW | 0x0 | 0 | 0x0 | 0 | 0 | 0x0 | Reset |
```

SLCHOST_SLCO_TOHOST_BITn_INT_RAW (n: 0-7) The raw interrupt status of SLCHOST_SLCO_TOHOST_BITn_INT (n: 0-7). (R/WTC/SS)

SLCHOST_SLCO_RX_UDF_INT_RAW The raw interrupt status of SLCHOST_SLCO_RX_UDF_INT. (R/WTC/SS)

SLCHOST_SLCO_TX_OVF_INT_RAW The raw interrupt status of SLCHOST_SLCO_TX_OVF_INT. (R/WTC/SS)

SLCHOST_SLCO_RX_NEW_PACKET_INT_RAW The raw interrupt status of SLCHOST_SLCO_RX_NEW_PACKET_INT. (R/WTC/SS)
```