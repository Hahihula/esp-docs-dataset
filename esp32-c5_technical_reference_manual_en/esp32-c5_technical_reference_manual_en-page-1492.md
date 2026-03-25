
```markdown
Register 39.44. SLCHOST_SLC1HOST_INT_ST_REG (0x005C)

| 31 | 26 | 25 | 24 | 18 | 17 | 16 | 15 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| (reserved) | SLCHOST_SLC1_RX_NEW_PACKET_INT_ST | (reserved) | SLCHOST_SLC1_TX_OVF_INT_ST | SLCHOST_SLC1_RX_UDF_INT_ST | SLCHOST_SLC1_TOHOST_BIT7_INT_ST | ... | SLCHOST_SLC1_TOHOST_BIT0_INT_ST |
| 0x0 | 0    | 0x0 | 0   | 0  | 0x0 | ... | 0x0 |

SLCHOST_SLC1_TOHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLCHOST_SLC1_TOHOST_BITn_INT (n: 0-7). (RO)

SLCHOST_SLC1_RX_UDF_INT_ST The masked interrupt status of SLCHOST_SLC1_RX_UDF_INT. (RO)

SLCHOST_SLC1_TX_OVF_INT_ST The masked interrupt status of SLCHOST_SLC1_TX_OVF_INT. (RO)

SLCHOST_SLC1_RX_NEW_PACKET_INT_ST The masked interrupt status of SLCHOST_SLC1_RX_NEW_PACKET_INT. (RO)


Register 39.45. SLCHOST_CONF_W7_REG (0x008C)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|
| SLCHOST_SLCHOST_CONF31 | (reserved) | ... | SLCHOST_SLCHOST_CONF29 | (reserved) |
| 0x0 | 0x0 | 0x0 | 0x0 |

SLCHOST_SLCHOST_CONF29 The interrupt set bits of SLCINT_SLC_FRHOST_BITn_INT (n: 0-7). These bits will not be cleared automatically. (R/W)

SLCHOST_SLCHOST_CONF31 The interrupt set bits of SLCINT_SLC_FRHOST_BITn_INT (n: 8-15). These bits will not be cleared automatically. (R/W)
```