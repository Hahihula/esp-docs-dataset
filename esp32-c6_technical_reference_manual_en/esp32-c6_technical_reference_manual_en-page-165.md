

```markdown
Register 4.33. GDMA_OUT_DSCR_BF1_CHn_REG (n: 0-2) (0x00F8+0xC0*n)

GDMA_OUTLINK_DSCR_BF1_CHn   Represents the address of the previous transmit descriptor y-1 that is pre-read. (RO)

Register 4.34. GDMA_IN_PRI_CHn_REG (n: 0-2) (0x009C+0xC0*n)

GDMA_RX_PRI_CHn    Configures the priority of RX channel n.
Value range: 0 ~ 9
The larger of the value, the higher of the priority. (R/W)

Register 4.35. GDMA_OUT_PRI_CHn_REG (n: 0-2) (0x00FC+0xC0*n)

GDMA_TX_PRI_CHn    Configures the priority of TX channel n.
Value range: 0 ~ 9
The larger of the value, the higher of the priority. (R/W)
```