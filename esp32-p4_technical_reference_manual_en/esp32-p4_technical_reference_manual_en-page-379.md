

```markdown
Register 5.13. DMAC_CHn_CFG0_REG (n: 1-4) (0x0100*/n + 0x0120)

| 31 |          ...          | 4 | 3 | 2 | 1 | 0 |
|----|------------------------|---|---|---|---|---|
| 0  | 0 0 0 0 0 0 0 0        | 0 | 0 | 0x0 | 0x0 | Reset |

DMAC_CHn_SRC_MULTBLK_TYPE Configures the source multi-block transfer type.
- 0: Contiguous address
- 1: Auto reloading
- 2: Shadow register
- 3: Linked list
(R/W)

DMAC_CHn_DST_MULTBLK_TYPE Configures the destination multi-block transfer type.
- 0: Contiguous address
- 1: Auto reloading
- 2: Shadow register
- 3: Linked list

If both DMAC_CHn_SRC_MULTBLK_TYPE and DMAC_CHn_DST_MULTBLK_TYPE are 0, then the transfer type is single-block transfer based on contiguous address.
(R/W)
```