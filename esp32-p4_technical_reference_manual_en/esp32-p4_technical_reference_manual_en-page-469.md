

```markdown
Register 6.62. DMA2D_OUT_PERI_SEL_CHn_REG (n: 0-3) (0x0038+0x100*n)

DMA2D_OUT_PERI_SEL_Ch_n   Configures the peripheral connected to TX channel n.

0: JPEG
1: SRM module of PPA
2: BLEND0 channel of PPA
3: BLEND1 channel of PPA
4 ~ 7: Dummy 4 ~ 7
(R/W)

Register 6.63. DMA2D_IN_PERI_SEL_CHn_REG (n: 0-2) (0x053C+0x100*n)

DMA2D_IN_PERI_SEL_Ch_n   Configures the peripheral connected to RX channel n.

0: JPEG
1: SRM module of PPA
2: BLEND module of PPA
3 ~ 7: Dummy 3 ~ 7
(R/W)
```