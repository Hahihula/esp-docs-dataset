

```markdown
## Register 3.43. AHB_DMA_OUT_DSCR_BF1_CHn_REG (n: 0-1) (0x00F8+0xC0*n)

```
AHB_DMA_OUTLINK_DSCR_BF1_CHn` Represents the address of the previous transmit descriptor y-1 that is pre-read. (RO)
```

## Register 3.44. AHB_DMA_IN_PRI_CHn_REG (n: 0-1) (0x009C+0xC0*n)

```
AHB_DMA_RX_PRI_CHn` Configures the priority of RX channel n. The larger the value, the higher the priority.
Value range: 0 ~ 5 (R/W)
```

## Register 3.45. AHB_DMA_OUT_PRI_CHn_REG (n: 0-1) (0x00FC+0xC0*n)

```
AHB_DMA_TX_PRI_CHn` Configures the priority of TX channel n. The larger the value, the higher the priority.
Value range: 0 ~ 5 (R/W)
```