

```markdown
Chapter 6 2D-DMA Controller (2D-DMA)

Register 6.8. DMA2D_OUT_SCRAMBLE_CHn_REG (n: 0-3) (0x004C+0x100*n)

DMA2D_OUT_SCRAMBLE_SEL_PRE_CHn Configures the byte order scrambling before the color space conversion for TX channel n.
0: BYTE2-1-O
1: BYTE2-O-1
2: BYTE1-O-2
3: BYTE1-2-O
4: BYTE0-2-1
5: BYTE0-1-2
Others: Invalid
(R/W)

Register 6.9. DMA2D_OUT_COLOR_PARAMO_CHn_REG (n: 0-3) (0x0050+0x100*n)

DMA2D_OUT_COLOR_PARAM_HO_CHn Configures the coefficient A and B for the most significant byte of the input of color space conversion's second stage for TX channel n. (R/W)
```