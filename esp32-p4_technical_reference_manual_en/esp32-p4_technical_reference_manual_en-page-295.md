

```markdown
Register 4.62. AHB_DMA_IN_PERI_SEL_CHn_REG (n: 0-2) (0x00A0+0xC0*n)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                        |
| 6   | 5      | 0       | Reset = 0x3f |

AHB_DMA_PERI_IN_SEL_CHn Configures the peripheral connected to RX channel n.

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
16 ~ 63: Invalid (R/W)
```