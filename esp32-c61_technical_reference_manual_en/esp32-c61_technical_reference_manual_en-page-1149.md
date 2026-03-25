

```markdown
Register 30.42. SLCHOST_SLC1HOST_INT_RAW_REG (0x0054)

| 31 | 26 | 25 | 24 | 18 | 17 | 16 | 15 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 0x0 |    |    | 0x0 |    |    |    | 0x0 | (reserved) | SLCHOST_SLC1_TOHOST_BIT7_INT_RAW | SLCHOST_SLC1_TOHOST_BIT6_INT_RAW | SLCHOST_SLC1_TOHOST_BIT5_INT_RAW | SLCHOST_SLC1_TOHOST_BIT4_INT_RAW | SLCHOST_SLC1_TOHOST_BIT3_INT_RAW | SLCHOST_SLC1_TOHOST_BIT2_INT_RAW | SLCHOST_SLC1_TOHOST_BIT1_INT_RAW | Reset |

SLCHOST_SLC1TOHOST_BITn_INT_RAW (n: 0-7) The raw interrupt status of SL-
CHOST_SLC1_TOHOST_BITn_INT (n: 0-7). (R/WTC/SS)

SLCHOST_SLC1_RX_UDF_INT_RAW The raw interrupt status of SLCHOST_SLC1_RX_UDF_INT.
(R/WTC/SS)

SLCHOST_SLC1_TX_OVF_INT_RAW The raw interrupt status of SLCHOST_SLC1_TX_OVF_INT.
(R/WTC/SS)

SLCHOST_SLC1_RX_NEW_PACKET_INT_RAW The raw interrupt status of SL-
CHOST_SLC1_RX_NEW_PACKET_INT. (R/WTC/SS)
```