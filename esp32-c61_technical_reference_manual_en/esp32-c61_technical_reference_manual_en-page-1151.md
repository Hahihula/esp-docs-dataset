

```markdown
## Register 30.44. SLCHOST_SLC1HOST_INT_ST_REG (0x005C)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                        |
| 26  | SLCHOST_SLC1_RX_NEW_PACKET_INT_ST                                                 |
| 24  | (reserved)                                                                        |
| 18  | SLCHOST_SLC1_TX_OVF_INT_ST                                                         |
| 17  | SLCHOST_SLC1_RX_UDF_INT_ST                                                        |
| 16  | SLCHOST_SLC1_RX_NEW_PACKET_INT_ST                                                 |
| 15  | (reserved)                                                                        |
| 8   | SLCHOST_SLC1_TOHOST_BITn_INT_ST (n: 0-7)                                          |
| 7   | SLCHOST_SLC1_TOHOST_BIT6_INT_ST                                                   |
| 6   | SLCHOST_SLC1_TOHOST_BIT5_INT_ST                                                   |
| 5   | SLCHOST_SLC1_TOHOST_BIT4_INT_ST                                                   |
| 4   | SLCHOST_SLC1_TOHOST_BIT3_INT_ST                                                   |
| 3   | SLCHOST_SLC1_TOHOST_BIT2_INT_ST                                                   |
| 2   | SLCHOST_SLC1_TOHOST_BIT1_INT_ST                                                   |
| 1   | SLCHOST_SLC1_TOHOST_BIT0_INT_ST                                                   |
| 0   | (reserved)                                                                        |

Reset: `0x0`

---

SLCHOST_SLC1_TOHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLCHOST_SLC1_TOHOST_BITn_INT. (RO)

SLCHOST_SLC1_RX_UDF_INT_ST The masked interrupt status of SLCHOST_SLC1_RX_UDF_INT. (RO)

SLCHOST_SLC1_TX_OVF_INT_ST The masked interrupt status of SLCHOST_SLC1_TX_OVF_INT. (RO)

SLCHOST_SLC1_RX_NEW_PACKET_INT_ST The masked interrupt status of SLCHOST_SLC1_RX_NEW_PACKET_INT. (RO)
```

```markdown
## Register 30.45. SLCHOST_CONF_W7_REG (0x008C)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | SLCHOST_SLCHOST_CONF31                                                             |
| 24  | (reserved)                                                                        |
| 23  | SLCHOST_SLCHOST_CONF31                                                             |
| 16  | (reserved)                                                                        |
| 15  | SLCHOST_SLCHOST_CONF29                                                             |
| 8   | SLCHOST_SLCHOST_CONF29                                                             |
| 7   | (reserved)                                                                        |
| 0   | Reset                                                                             |

Reset: `0x0`

---

SLCHOST_SLCHOST_CONF29 The interrupt set bits of SLCINT_SLC_FRHOST_BITn_INT (n: 0-7). These bits will not be cleared automatically. (R/W)

SLCHOST_SLCHOST_CONF31 The interrupt set bits of SLCINT_SLC_FRHOST_BITn_INT (n: 8-15). These bits will not be cleared automatically. (R/W)
```