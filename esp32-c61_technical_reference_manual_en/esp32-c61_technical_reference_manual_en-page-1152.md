
```markdown
Register 30.46. SLCHOST_SLCOHOST_INT_CLR_REG (0x00D4)

| 31 | 24 | 23 | 22 | (reserved) | 18 | 17 | 16 | 15 | (reserved) | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|------------:|----:|----:|----:|----:|------------:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|    |   0 |   0 | 0x0 |           0 |   0 |   0 |   0 | 0x0 |            (reserved) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SLCHOST_SLCO_TOHOST_BITn_INT_CLR (n: 0-7) Write 1 to clear interrupt SL-
CHOST_SLCO_TOHOST_BITn_INT (n: 0-7). (WT)

SLCHOST_SLCO_RX_UDF_INT_CLR Write 1 to clear interrupt SLCHOST_SLCO_RX_UDF_INT. (WT)

SLCHOST_SLCO_TX_OVF_INT_CLR Write 1 to clear interrupt SLCHOST_SLCO_TX_OVF_INT. (WT)

SLCHOST_SLCO_RX_NEW_PACKET_INT_CLR Write 1 to clear interrupt SL-
CHOST_SLCO_RX_NEW_PACKET_INT. (WT)


Register 30.47. SLCHOST_SLC1HOST_INT_CLR_REG (0x00D8)

| 31 | 26 | 25 | 24 | (reserved) | 18 | 17 | 16 | 15 | (reserved) | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|------------:|----:|----:|----:|----:|------------:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|    |   0 |   0 | 0x0 |           0 |   0 |   0 |   0 | 0x0 |            (reserved) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SLCHOST_SLC1_TOHOST_BITn_INT_CLR (n: 0-7) Write 1 to clear interrupt SL-
CHOST_SLC1_TOHOST_BITn_INT (n: 0-7). (WT)

SLCHOST_SLC1_RX_UDF_INT_CLR Write 1 to clear interrupt SLCHOST_SLC1_RX_UDF_INT. (WT)

SLCHOST_SLC1_TX_OVF_INT_CLR Write 1 to clear interrupt SLCHOST_SLC1_TX_OVF_INT. (WT)

SLCHOST_SLC1_RX_NEW_PACKET_INT_CLR Write 1 to clear interrupt SL-
CHOST_SLC1_RX_NEW_PACKET_INT. (WT)
```