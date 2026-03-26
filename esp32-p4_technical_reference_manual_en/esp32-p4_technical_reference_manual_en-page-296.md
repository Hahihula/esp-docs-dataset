

```markdown
Register 4.63. AHB_DMA_OUT_PERI_SEL_CHn_REG (n: 0-2) (0x0100+0xC0*n)

| 31 | 30 | 29 | 28 | ... | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|-----|---|---|---|---|---|---|
| 0  | 0  | 0  | 0  | ... | 0 | 0 | 0 | 0 | 0x3f | Reset |

AHB_DMA_PERI_OUT_SEL_CHn Configures the peripheral connected to TX channel n.

0: I3C
1: Dummy-1
2: UHCI
3: I2SO
4: I2S1
5: I2S2
6: Dummy-6
7: Dummy-7
8: ADC
9: Dummy-9
10: RMT
11 ~ 15: Dummy-11 ~ Dummy-15
16 ~ 63: Invalid
(R/W)
```