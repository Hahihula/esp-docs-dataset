

```markdown
Chapter 19 Permission Control (PMS)

Register 19.37. PMS_DMA_GMAC_PMS_R_REG (0x01B4)

| 31 | 0 |
|-----|----|
|     |    |

0xffffff Reset

PMS_DMA_GMAC_R_PMS Configures read permission for EMAC to access 32 address ranges. Bit
0 corresponds to region0, and so on.
0: Disable read permission.
1: Enable read permission.
(R/W)

Register 19.38. PMS_DMA_GMAC_PMS_W_REG (0x01B8)

| 31 | 0 |
|-----|----|
|     |    |

0xffffff Reset

PMS_DMA_GMAC_W_PMS Configures write permission for EMAC to access 32 address ranges. Bit
0 corresponds to region0, and so on.
0: Disable write permission.
1: Enable write permission.
(R/W)
```