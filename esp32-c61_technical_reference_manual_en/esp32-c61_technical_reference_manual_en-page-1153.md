

```markdown
Register 30.48. SLCHOST_SLCOHOST_FUNC1_INT_ENA_REG (0x00DC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    | reserved) | SLCHOST_FN1_SLC0_TOHOST_BITn_INT_ENA (n: 0-7) Write 1 to enable SLCHOST_SLC0_TOHOST_BITn_INT (n: 0-7). (R/W) | reserved) | SLCHOST_FN1_SLC0_RX_NEW_PACKET_INT_ENA |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |
| Value | 0x0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

SLCHOST_FN1_SLC0_TOHOST_BITn_INT_ENA (n: 0-7) Write 1 to enable SLCHOST_SLC0_TOHOST_BITn_INT (n: 0-7). (R/W)

SLCHOST_FN1_SLC0_RX_UDF_INT_ENA Write 1 to enable SLCHOST_SLC0_RX_UDF_INT. (R/W)

SLCHOST_FN1_SLC0_TX_OVF_INT_ENA Write 1 to enable SLCHOST_SLC0_TX_OVF_INT. (R/W)

SLCHOST_FN1_SLC0_RX_NEW_PACKET_INT_ENA Write 1 to enable SLCHOST_SLC0_RX_NEW_PACKET_INT. (R/W)


Register 30.49. SLCHOST_SLC1HOST_FUNC1_INT_ENA_REG (0x00E0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | reserved) | SLCHOST_FN1_SLC1_RX_NEW_PACKET_INT_ENA |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |
| Value | 0x0 | 0 | 0x0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

SLCHOST_FN1_SLC1_TOHOST_BITn_INT_ENA (n: 0-7) Write 1 to enable SLCHOST_SLC1_TOHOST_BITn_INT (n: 0-7). (R/W)

SLCHOST_FN1_SLC1_RX_UDF_INT_ENA Write 1 to enable SLCHOST_SLC1_RX_UDF_INT. (R/W)

SLCHOST_FN1_SLC1_TX_OVF_INT_ENA Write 1 to enable SLCHOST_SLC1_TX_OVF_INT. (R/W)

SLCHOST_FN1_SLC1_RX_NEW_PACKET_INT_ENA Write 1 to enable SLCHOST_SLC1_RX_NEW_PACKET_INT. (R/W)
```